<template>
  <div id="app">
    <!-- displaying the navigation component -->
    <Navigation msg="This is a navigation" />
  </div>
</template>

<script>
// importing navigation
import Navigation from "./components/Navigation.vue";
export default {
  components: {
    Navigation
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.home,
.about,
.contact,
.testimonials {
  margin-top: 60px;
}
</style>
