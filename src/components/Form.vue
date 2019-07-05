<template>
  <div id="form">
    <form @submit.prevent="addComment">
      <div id="formEl">
        <input type="text" placeholder="Your Name" v-model="newName" />
      </div>
      <div id="formEl">
        <input type="text" placeholder="Your Job Title" v-model="newJob" />
      </div>
      <div id="formEl">
        <input
          type="textarea"
          placeholder="Your Comment"
          v-model="newComment"
        />
      </div>
      <input type="submit" value="Submit" />
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      newName: "",
      newJob: "",
      newComment: ""
    };
  },
  methods: {
    addComment() {
      const someObj = {
        name: this.newName,
        position: this.newJob,
        comment: this.newComment
      };
      this.$emit("newComment", someObj);
      if (this.newComment.length < 50) {
        someObj.comment = this.newComment;
        this.newComment = "";
      } else {
        alert("All the fields are required");
      }
      if (this.newName.length) {
        someObj.name = this.newName;
        this.newName = "";
      } else {
        alert("All the fields are required");
      }
      if (this.newJob.length) {
        this.newJob = "";
      } else {
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
