<template>
  <div class="container">
    <h3>{{ title }}</h3>
    <slot> </slot>
  </div>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border: 1px solid peachpuff;
  border-radius: 22px;
}

.container :hover {
  background: rgb(26, 26, 26);
}
</style>