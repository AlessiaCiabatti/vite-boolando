<script>
  export default {
    props:{
      frontImage: String
    }
  }
</script>



<template>


  <!-- prima immagine -->
  <div class="prodotto-uno">
    <!-- non sono p ma span -->
    <p class="sconto">50%</p>
    <p class="sostenibilità">Sostenibilità</p>

    <img :src="frontImage">
    <!-- <img class="img-none" src="img/1b.webp" alt=""> -->
    <p class="marca-prodotto">Levi's</p>
    <!-- anche questi sono span non p e la scritta principale è strong-->
    <p>RELAXED FIT TEE UNISEX</p>
    <P class="prezzo-offerta">14,99&#8364;<span class="prezzo-originale"> 29,99&#8364;</span></P>
    <div class="heart">
    <span>&hearts;</span>
    </div>
  </div>


</template>



<style lang="scss">

  .prodotto-uno {
    position: relative;
    height: 530px;
    width: calc(100vw / 3);
    margin-bottom: 20px;
  }

.container .prodotto-uno{
  height: 530px;
  width: 335px;
}

.prodotto-uno .sconto{
  position: absolute;
  bottom: 60px;
  background-color: #ff0000;
  padding: 3px 8px;
  color: white;
  z-index: 1
}

.prodotto-uno .sostenibilità{
  position: absolute;
  bottom: 60px;
  left: 45px;
  background-color: #008000;
  padding: 3px 8px;
  color: white;
  z-index: 1
}

.prodotto-uno .heart:hover{
  color: #ff0000;
  cursor: pointer;
}

.prodotto-uno .heart{
  position: absolute;
  top: 10px;
  right: 0px;
  font-size: 25px;
  background-color: white;
  padding: 5px 10px;
}

.prodotto-uno img{
  width: 100%;
}
</style>