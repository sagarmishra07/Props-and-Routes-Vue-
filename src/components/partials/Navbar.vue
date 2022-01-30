<template>
  <nav>
    <router-link :to="{ name: 'Home' }"><li>Home</li></router-link>
    <router-link :to="{ name: 'Product' }"><li>Products</li></router-link>

    <router-link :to="{ name: 'About' }"><li>About</li></router-link>
  </nav>
</template>
<script>
export default {
  name: "Navbar",
};
</script>
<style scoped>
* {
  margin: 1%;
}
nav {
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding-bottom: 2%;
  font-size: 35px;
  background: lavenderblush;
}

li {
  list-style: none;
}
</style>