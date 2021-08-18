<template>
  <div class="container">
    <the-header
      class="viewport-header"
      @selected="changeComponent"
    ></the-header>
    <div class="body">
      <transition name="fade">
        <component :is="getComponent()"> </component>
      </transition>
    </div>
  </div>
</template>

<script>
import TheHeader from "../components/ui/TheHeader.vue";
import HomeBody from "../components/HomeBody.vue";
import SkillsBody from "../components/SkillsBody.vue";
import ProjectsBody from "../components/ProjectsBody.vue";

export default {
  components: { TheHeader, HomeBody, SkillsBody, ProjectsBody },
  data() {
    return {
      selectedComponent: "home",
      mapping: {
        home: "HomeBody",
        skills: "SkillsBody",
        projects: "ProjectsBody",
      },
    };
  },
  methods: {
    getComponent() {
      return this.mapping[this.selectedComponent];
    },
    changeComponent(arg) {
      console.log("Changing ", this.selectedComponent, " to ", this.arg);
      this.selectedComponent = arg;
    },
  },
};
</script>

<style scoped>
video {
  object-fit: cover;
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
}

.viewport-header {
  position: relative;
}

.container {
  background: black;
  height: 100%;
}

.body {
  min-height: 100vh;
}
</style>
