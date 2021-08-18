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
@keyframes fade {
  from {
    opacity: 0;
  }
  to {
    opacity: 100;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
