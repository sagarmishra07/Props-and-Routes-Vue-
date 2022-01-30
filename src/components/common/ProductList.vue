<template>
  <div class="card-item">
    <h1>{{ product.name }}</h1>
    <img :src="product.image" alt="No Image" />
    <h2>{{ product.description }}</h2>
    <p>Rs.{{ product.price }}</p>
    <button>
      <router-link :to="{ name: 'SingleProduct', params: { id: product.id } }"
        >View Details</router-link
      >
    </button>
  </div>
</template>
<script>
export default {
  name: "ProductList",
  props: {
    product: Object,
  },
};
</script>
<style scoped>
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
  margin: 0rem 0rem 0rem 6rem;

  font-size: 1.3rem;
}
h3 {
  color: aliceblue;
}
router-link a {
  text-decoration: none;
}
</style>