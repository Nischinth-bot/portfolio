<template>
  <div class="container"><home-page> </home-page></div>
  <the-footer> </the-footer>
</template>

<script>
import TheFooter from "./components/ui/TheFooter.vue";
import HomePage from "./pages/HomePage.vue";

export default {
  name: "App",
  components: {
    HomePage,
    TheFooter,
  },
};
</script>

<style>
html,
body {
  height: 100%;
  background: black;
  color: white;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
