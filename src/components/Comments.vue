<template>
  <div id="comms">
    <div class="post" v-for="comment in comments">
      <b>
        <p>{{ comment.name }} - {{ comment.position }}</p>
      </b>
      <p>{{ comment.comment }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    comments: {
      type: Array,
      required: true
    }
  }
};
</script>
<style>
#comms {
  display: inline-grid;
  grid-template-columns: 25% 25% 25% 25%;
  grid-template-rows: auto;
}

.post {
  border: 1px solid grey;
  width: 300px;
  margin: 10px;
}
</style>
