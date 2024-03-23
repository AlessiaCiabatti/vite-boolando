<script>
  export default {
    props:{
      brand: String,
      name: String,
      price: String,
    },
  }
</script>

<template>
  <p class="marca-prodotto">{{brand}}</p>
  <!-- anche questi sono span non p e la scritta principale è strong-->
  <p class="name">{{name}}</p>
  <P class="prezzo-offerta">{{price}}&#8364;</P>
  <div class="heart">
    <span>&hearts;</span>
  </div>
</template>

<style lang="scss">
@use '../../assets/scss/partials/variables' as *;

.prodotto-uno,p{
  font-size: 12px;
  .marca-prodotto{
    color: $marca-color;
    font-size: 15px;
  }
}

</style>