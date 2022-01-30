<template>
  <div v-for="product in value" :key="product.id" class="container">
    <div class="card-item">
      <h1>{{ product.name }}</h1>
      <img :src="product.image" alt="No Image" />
      <h2>{{ product.description }}</h2>
      <p>Rs.{{ product.price }}</p>
    </div>
  </div>
</template>
<script>
import { ALL_PRODUCTS } from "@/utils/MockData/Products";
export default {
  name: "SingleProduct",
  data() {
    return {
      id: this.$route.params.id,
      Products: [],
    };
  },
  created() {
    this.Products = ALL_PRODUCTS;
  },
  computed: {
    value() {
      return this.Products.filter((pro) => pro.id == this.id);
    },
  },
};
</script>
<style scoped>
.container {
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  align-content: center;
}

img {
  height: 20rem;
  width: 20rem;
  display: flex;
  justify-content: center;
  align-content: center;
}
.card-item {
  background: lavenderblush;
}
h1,
h2,
p {
  display: flex;
  justify-content: center;
  text-align: center;
}
button {
  background: teal;

  display: grid;
  place-items: center;
  font-size: 1.3rem;
}
h3 {
  color: aliceblue;
}
router-link a {
  text-decoration: none;
}
</style>>
