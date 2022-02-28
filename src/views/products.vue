<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <products />
  </div>
</template>

<script>
// @ is an alias to /src
import Landing from "@/src/products.js";

export default {
  name: "Home",
  components: {
    products,
  },
};
</script>

<style scoped>
#products {
  flex-wrap: wrap;
}

#products img {
  height: 300px;
  object-fit: contain;
}

.card {
  width: calc(100% / 4);
  margin-bottom: 10px;
  margin-right: 5px;
}

</style>