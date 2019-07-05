<template>
  <!-- form -->
  <div id="form">
    <form @submit.prevent="addComment">
      <!-- name field -->
      <div id="formEl">
        <input
          type="text"
          maxlength="50"
          placeholder="Your Name"
          v-model="newName"
        />
      </div>
      <!-- job title field -->
      <div id="formEl">
        <input
          type="text"
          maxlength="50"
          placeholder="Your Job Title"
          v-model="newJob"
        />
      </div>
      <!-- comment field -->
      <div id="formEl">
        <input
          type="textarea"
          maxlength="120"
          placeholder="Your Comment"
          v-model="newComment"
        />
      </div>
      <!-- submit button -->
      <input type="submit" value="Submit" />
    </form>
  </div>
</template>
<script>
export default {
  data() {
    // return input values
    return {
      newName: "",
      newJob: "",
      newComment: ""
    };
  },
  methods: {
    // adding the comment
    addComment() {
      const someObj = {
        name: this.newName,
        position: this.newJob,
        comment: this.newComment
      };
      // validating that fields are not empty
      this.$emit("newComment", someObj);
      if (this.newComment.length) {
        someObj.comment = this.newComment;
        this.newComment = "";
      } else {
        this.newComment = "";
        alert("All the fields are required");
      }
      if (this.newName.length) {
        someObj.name = this.newName;
        this.newName = "";
      } else {
        this.newName = "";
        alert("All the fields are required");
      }
      if (this.newJob.length) {
        this.newJob = "";
      } else {
        this.newJob = "";
        alert("All the fields are required");
      }
    }
  }
};
</script>
<style scoped>
input {
  min-width: 200px;
  padding: 10px 20px;
  font-size: 1.5rem;
}

#form {
  display: flex;
  flex-direction: column;
}

#formEl {
  margin: 10px;
}
</style>
