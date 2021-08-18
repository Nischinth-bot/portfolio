<template>
  <div class="container">
    <h3>{{ title }}</h3>
    <p>{{ desc }}</p>
  </div>
</template>

<script>
export default {
  props: [{ title: String }, { desc: String }, { imgs: Array }],
};
</script>
