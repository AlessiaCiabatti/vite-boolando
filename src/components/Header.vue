<script>
  export default {
    
  }
</script>

<template>
  <header>
    <div class="container-header">
      <div class="nav">

        <div class="menu">
          <ul>
            <li>
              <a href="#">Donna</a>
            </li>
            <li>
              <a href="#">Uomo</a>
            </li>
            <li>
              <a href="#">Bambini</a>
            </li>
          </ul>
        </div>

        <div class="logo">
          <img src="../assets/img/boolean-logo.png" alt="Logo">
        </div>

        <div class="icone">
          <div>
            <i class="fa-regular fa-user"></i>
            <i class="fa-regular fa-heart"></i>
            <i class="fa-solid fa-bag-shopping"></i>
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
}

.container-header{
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
  }
}

.menu{
  ul{
    li{
      a{
        text-decoration: none;
        padding-right: 7px;
        color: $icon-color;
      }
    }
  }
}

.container-header{
  .logo{
    text-align: center;
  }
}

.container-header {
  .logo{
    flex-grow: 1;
  }
}

.logo{
  img{
    height: 20px;
  }
}

.icone{
  .fa-regular{
    padding-right: 8px;
  }
} 
</style>