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
@use '../../assets/scss/partials/variables' as *;

.prodotto-uno {
  position: relative;
  height: 530px;
  width: 335px;
  margin-bottom: 20px;
  .badges{
    position: absolute;
    bottom: 65px;
    color: $writen-color;
    z-index: 1;
  }
  img{
    width: 100%;
  }
  .img-none{
    position: absolute;
    top: 0px;
    left: 0px;
    display: none;
  }
  .heart{
    position: absolute;
    top: 10px;
    right: 0px;
    font-size: 20px;
    background-color: $writen-color;
    padding: 5px 10px;
  }
}

span.discount{
  background-color: $heart-color;
  padding: 3px 8px;
}

span.tag{
  background-color: $sostenibile-g;
  padding: 3px 8px;
  margin-right: 10px;
}

// .prodotto-uno .heart:hover{
//   color: #ff0000;
//   cursor: pointer;
// }


.prodotto-uno:hover .img-none{
  display: inline-block;
}

</style>