<template>
  <div class="home">
    <h1>{{ title }}</h1>
    <div class="content">
      <div id="imgOne"></div>
      <div id="text">
        {{ textOne }}
        <br />
        <br />
        {{ textTwo }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Welcome To My Vue App",
      textOne:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Elementum integer enim neque volutpat ac. Vitae et leo duis ut. Ac turpis egestas sed tempus. Viverra nam libero justo laoreet sit amet. Odio aenean sed adipiscing diam donec. Lacus suspendisse faucibus interdum posuere lorem. Fermentum dui faucibus in ornare quam viverra. Nec sagittis aliquam malesuada bibendum.",
      textTwo:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Elementum integer enim neque volutpat ac. Vitae et leo duis ut. Ac turpis egestas sed tempus. Viverra nam libero justo laoreet sit amet. Odio aenean sed adipiscing diam donec. Lacus suspendisse faucibus interdum posuere lorem."
    };
  }
};
</script>
<style>
#imgOne {
  height: 300px;
  width: 300px;
  background-color: #534061;
}
</style>
