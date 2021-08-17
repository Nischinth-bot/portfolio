<template>
  <div class="container">
    <h3>{{ title }}</h3>
  </div>
</template>

<script>
export default {
  props: [{ title: String }, { imgs: Array }],
};
</script>
