<template>
  <div class="about">
    <h1>{{ title }}</h1>
    <div class="contentAbout">
      <!-- section one -->
      <div class="section">
        <!-- image -->
        <div id="imgTwo"></div>
        <!-- text -->
        <div id="text">{{ textOne }}</div>
      </div>
      <!-- section two -->
      <div class="section two">
        <!-- text -->
        <div id="textTwo">{{ textTwo }}</div>
        <!-- image -->
        <div id="imgTwo"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // return data for the page
      title: "About The Vue App",
      textOne:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Elementum integer enim neque volutpat ac. Vitae et leo duis ut. Ac turpis egestas sed tempus. Viverra nam libero justo laoreet sit amet. Odio aenean sed adipiscing diam donec.",
      textTwo:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna consectetur adipiscing elit aliqua. Elementum integer enim neque volutpat ac. Vitae et leo duis ut. Ac turpis egestas sed tempus."
    };
  }
};
</script>
<style>
.section {
  display: flex;
  flex-direction: row;
}
#imgTwo {
  height: 150px;
  width: 300px;
  background-color: #534061;
}
.two {
  margin-top: 50px;
}

#textTwo {
  text-align: left;
  width: 50%;
  margin-right: 40px;
}

.contentAbout {
  margin-top: 70px;
  width: 60%;
  margin-left: 20%;
}
</style>
