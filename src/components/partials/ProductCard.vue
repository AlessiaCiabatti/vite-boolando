<script>
import BottomCard from '../partials/BottomCard.vue';
  export default {
    props: {
    frontImage: String,
    badges: Array,
    brand: String,
    name: String,
    price: String,
    },
    data(){
    
    },
    components:{
        BottomCard
      }
  }
</script>



<template>


  <!-- prima immagine -->
  <div class="prodotto-uno">
    <!-- non sono p ma span -->
    <!-- <p class="sconto">50%</p> -->
    <div  class="badges">
      <span v-for="(badge, index) in badges" 
      :key="index" :class="badge.type">
        {{ badge.value }}
      </span>
    </div>
    <img :src="frontImage">
    <!-- <img class="img-none" src="img/1b.webp" alt=""> -->
    
    <BottomCard 
    :brand="brand" 
    :name="name" 
    :price="price" />

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

.prodotto-uno .badges{
  position: absolute;
  bottom: 65px;
  // left: 45px;
  // background-color: #008000;
  color: white;
  z-index: 1;
}

span.discount{
  background-color: #ff0000;
  padding: 3px 8px;
}

span.tag{
  background-color: #008000;
  padding: 3px 8px;
  margin-right: 10px;
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

.prodotto-uno .img-none{
  position: absolute;
  top: 0px;
  left: 0px;
  display: none;
}

.prodotto-uno:hover .img-none{
  display: inline-block;
}

.prodotto-uno .six{
  position: absolute;
  left: 0px;
}
</style>