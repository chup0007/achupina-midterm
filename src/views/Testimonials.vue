<template>
  <div>
    <h1>{{ title }}</h1>
    <Comments :comments="commentsList" />
    <Form @newComment="addComment" />
  </div>
</template>
<script>
// importing components
import Comments from "@/components/Comments.vue";
import Form from "@/components/Form.vue";

// We will simply need to import axios since it a node package we do not need to specify a file.
import axios from "axios";

export default {
  components: {
    Comments,
    Form
  },
  data() {
    return {
      // array for the comments
      commentsList: [],
      title: "Testimonials"
    };
  },
  methods: {
    // adding new valid comment to the array
    addComment(comment) {
      this.commentsList.push(comment);

      // Making an axios put request to send the todoList array to Firebase
      axios
        .put("https://chup0007.firebaseio.com/data.json", this.commentsList)
        .then(response => {
          // we are logging the status message on success
          console.log("Your data was saved status: " + response.status);
        })
        .catch(error => {
          // we are logging the error message
          console.log("There was an error in saving data: " + error.response);
        });
    }
  },
  // created is a life cycle hook which will run when the instance is created
  created() {
    // here we are making a GET request using AXIOS to get the data
    axios
      .get("https://chup0007.firebaseio.com/data.json")
      .then(response => {
        // console.log(response);
        // console.log(response.data);

        // Checking if the response has some data
        if (response.data) {
          this.namesList = response.data;
          this.jobsList = response.data;
          this.commentsList = response.data;
        }
      })
      .catch(error => {
        console.log("There was an error in getting data: " + error.response);
      });
  }
};
</script>
<style>
ul {
  list-style: none;
  width: 50%;
  margin: 0 auto;
}
ul li {
  border-bottom: 1px solid #acacac;
  padding: 10px 0;
  margin-bottom: 10px;
}
</style>
