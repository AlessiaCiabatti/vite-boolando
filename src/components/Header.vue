<script>
  export default {
    data(){
      return{
        arrayNav: [
          {
            text: 'Uomo',
            href: '#'
          },
          {
            text: 'Donna',
            href: '#'
          },
          {
            text: 'Bambino',
            href: '#'
          },
        ],
        arrayIcone: ['fa-regular fa-user', 'fa-regular fa-heart', 'fa-solid fa-bag-shopping']
      }
    }
    
  }
</script>

<template>
  <header>
    <div class="container-header">
      <div class="nav">

        <div class="menu">
          <ul>
            <li v-for="(scelta, index) in arrayNav"
            :key="`nav-${index}`">
              <a :href="scelta.href">{{scelta.text}}</a>
            </li>
            <!-- <li>
              <a href="#">Uomo</a>
            </li>
            <li>
              <a href="#">Bambini</a>
            </li> -->
          </ul>
        </div>

        <div class="logo">
          <img src="../assets/img/boolean-logo.png" alt="Logo">
        </div>

        <div class="icone">
          <!-- ciclo for e :class="nome" -->
          <div>
            <i v-for="icona in arrayIcone" :class="icona"></i>
            <!-- <i class="fa-regular fa-heart"></i>
            <i class="fa-solid fa-bag-shopping"></i> -->
          </div>
        </div>

      </div>
    </div>
  </header>
</template>


<style lang="scss">
// per far funzionare le variabili devo richiamarle
@use '../assets/scss/partials/variables' as *;

.container-header{
  background-color: $bg-header;
  height: 55px;
  .nav{
    display: flex;
    align-items: center;
    height: 55px;
    max-width: 1030px;
    margin: 0 auto;
    color: $icon-color;
    font-size: 12px;
  }
}

.menu{
  ul{
    list-style: none;
    display: flex;
    li{
      a{
        text-decoration: none;
        padding-right: 7px;
        color: $icon-color;
        &:hover{
          text-decoration: underline;
        }
      }
    }
  }
}

.container-header{
  .logo{
    text-align: center;
    flex-grow: 1;
    img{
      height: 20px;
    }
  }
}

.icone {
  i {
    cursor: pointer;
  }
  .fa-regular{
    padding-right: 8px;
  }
}



</style>