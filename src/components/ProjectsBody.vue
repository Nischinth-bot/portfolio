<template>
  <div class="container">
    <ul class="all-projects">
      <li class="project">
        <h1>FLIPBITS</h1>
        <p class="desc">
          I designed and implemented an ecommerce application from scratch using
          Vue.js, HTML5, CSS3 and Firebase. <br />
          Features include carts, inventory management, OAuth and merchant
          specific features.
        </p>
        <a href="https://github.com/Nischinth-bot/flipbits4cs" target="_blank">
          <img class="small" src="../assets/github.png" />
        </a>
        <button v-if="!showMore" @click="showMore = true">Show More</button>
        <button v-if="showMore" @click="showMore = false">Show Less</button>
        <div v-if="showMore">
          <ul class="icons">
            <li class="icon">
              <img src="@/assets/eshop1.png" />
            </li>
            <li class="icon">
              <img src="@/assets/eshop2.png" />
            </li>
          </ul>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMore: true,
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}

.container * {
  list-style: none;
}
.container .all-projects {
  display: flex;
  flex-direction: column;
  margin-right: 2rem;
}

.all-projects .project {
  border: 1px solid peachpuff;
  border-radius: 22px;
}

button {
  margin: 1rem;
  font-size: 20px;
  color: white;
  background: rgb(89, 3, 89);
  border: 1px solid black;
  border-radius: 22px;
  padding: 0.5rem;
  cursor: pointer;
}

.small {
  height: 25px;
  width: 25px;
  padding: 0.25rem;
}

img {
  max-height: 500px;
  max-width: 100%;
}

h1 {
  border-bottom: purple 1px solid;
  width: 25%;
}
</style>
