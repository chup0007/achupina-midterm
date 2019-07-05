<template>
  <div>
    <div id="nav">
      <div id="title">
        <h2>My Vue App</h2>
      </div>
      <div id="menu">
        <router-link :to="{ name: 'home' }">Home</router-link>
        <router-link :to="{ name: 'about' }">About</router-link>
        <router-link :to="{ name: 'contact' }">Contact</router-link>
        <router-link :to="{ name: 'testimonials' }">Testimonials</router-link>
      </div>
    </div>
    <router-view />
    <footer>{{ copyright }}</footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      copyright: "Copyright My Vue App 2019"
    };
  }
};
</script>
<style>
#nav,
footer {
  background-color: #705f7d;
  padding: 30px;
  color: #d9c9e5;
  font-size: 20px;
}

footer {
  position: absolute;
  padding: 15px;
  width: 98%;
  bottom: 0;
  margin-top: 20px;
}
#menu {
  margin-left: 700px;
  display: flex;
  justify-content: space-between;
  width: 550px;
}
#title {
  width: 300px;
  margin-top: -25px;
  position: absolute;
}
#nav a {
  font-weight: bold;
  color: #d9c9e5;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #534061;
}

.content {
  margin-top: 70px;
  display: flex;
  flex-direction: row;
  margin-left: 20%;
  width: 60%;
}

#text {
  margin-left: 50px;
  text-align: left;
  width: 50%;
}
</style>
