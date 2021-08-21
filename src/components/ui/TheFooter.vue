<template>
  <div class="container">
    <div class="footer">
      <div class="pics">
        <img src="../../assets/linkedin.png" />
        <img src="../../assets/github.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  display: flex;
  width: 100%;
  background: rgb(2, 0, 36);
  background: linear-gradient(
    90deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(63, 17, 77, 1) 33%,
    rgba(42, 25, 47, 1) 90%
  );
  color: white;
  padding: 0.5rem;
  margin-top: 2rem;
  height: 200px;
  flex-direction: column;
}
.name {
  margin-top: auto;
  margin-left: auto;
  border: 1px solid white;
}

.icons {
  align-self: center;
}

.pics {
  display: flex;
  align-self: center;
  margin-top: auto;
  margin-bottom: auto;
  width: 10rem;
  justify-content: space-between;
}
.pics img {
  height: 50px;
  width: 50px;
}
</style>
