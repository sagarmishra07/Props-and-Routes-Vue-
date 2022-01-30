<template>
  <div class="container">
    <div v-for="product in Products" :key="product.id" class="product">
      <div class="card">
        <ProductList :product="product" />
      </div>
    </div>
  </div>
</template>
<script>
import ProductList from "../components/common/ProductList.vue";
import { ALL_PRODUCTS } from "@/utils/MockData/Products";
export default {
  name: "Product",
  components: {
    ProductList,
  },

  data() {
    return {
      Products: [],
    };
  },
  created() {
    this.Products = ALL_PRODUCTS;
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

.card {
  padding: 0rem 3rem 0rem 0rem;
}
</style>