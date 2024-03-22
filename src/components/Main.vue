<script>
import ProductCard from './partials/ProductCard.vue';
import products from '../assets/data/products';


  export default {
    data(){
      return {
        products
      }
    },
    components:{
      ProductCard
    },
    mounted(){
      console.log(products)
    }
  }
</script>

<template>
  <div class="container">
    <ProductCard 
    v-for="product in products"
    :key="product.id"
    :frontImage="`/src/assets/img/${product.frontImage}`"
    :brand="product.brand"
    :name="product.name"
    :price="product.price"/>
    <!-- <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard /> -->
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