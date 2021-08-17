<template>
  <div class="container">
    <ul class="header-items">
      <li class="item" @click="selectAndEmit('home')" :class="getClass('home')">
        Home
      </li>
      <li
        class="item"
        @click="selectAndEmit('skills')"
        :class="getClass('skills')"
      >
        Skills
      </li>
      <li
        class="item"
        @click="selectAndEmit('projects')"
        :class="getClass('projects')"
      >
        Projects
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  emits: ["selected"],
  data() {
    return {
      selectedComponent: "home",
    };
  },
  computed: {},
  methods: {
    selectAndEmit(arg) {
      this.selectedComponent = arg;
      this.$emit("selected", arg);
    },
    getClass(arg) {
      if (this.selectedComponent === arg) {
        return "item-underline";
      }
      return "item";
    },
  },
};
</script>

<style scoped>
.container {
}

.header-items {
  list-style: none;
  display: flex;
  justify-content: center;
  cursor: pointer;
  color: white;
}
.item:hover {
  border-bottom: 1px solid white;
}
.item {
  margin: 1rem;
  padding: 1rem;
  font-size: 25px;
}

.item-underline {
  border-bottom: 1px solid white;
}
</style>
