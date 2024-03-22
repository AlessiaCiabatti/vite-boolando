<script>
import ProductCard from './partials/ProductCard.vue';
  export default {
    components:{
      ProductCard
    }
  }
</script>

<template>
  <div class="container">
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
  </div>

</template>

<style lang="scss">
@use '../assets/scss/partials/variables' as *;

.container{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  max-width: 1030px;
  margin: 50px auto;
  }

</style>