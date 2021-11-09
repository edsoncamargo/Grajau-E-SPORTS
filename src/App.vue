<template>
  <main>
    <Navbar></Navbar>
    <Home></Home>
    <Trophies></Trophies>
    <Shields></Shields>
  </main>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";
import Trophies from "./components/Trophies.vue";
import Shields from "./components/Shields.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
    Trophies,
    Shields,
  },
};
</script>

<style lang="scss">
#app {
  @import url("https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
  @import url("https://fonts.googleapis.com/css2?family=Raleway:wght@500&display=swap");
  font-family: "Raleway", sans-serif;
}
</style>
