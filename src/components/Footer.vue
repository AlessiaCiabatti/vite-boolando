<script>
  export default {
    
  }
</script>

<template>
<div class="container-footer">
    <div class="text-footer">
      <div class="boolando">
        <h4>Boolando s.r.l.</h4>
        <div class="menu">
          <ul>
            <li>
              <a href="#">Informazioni legali</a>
            </li>
            <li>
              <a href="#">Informativa sulla privacy</a>
            </li>
            <li>
              <a href="#">Diritto di recesso</a>
            </li>
          </ul>
        </div>
      </div>

      <div class="social">
        <div class="trovaci">
          <h4>Trovaci anche su</h4>
          <div class="icone-footer">
            <i class="fa-brands fa-square-twitter"></i>
            <i class="fa-brands fa-square-facebook"></i>
            <i class="fa-brands fa-square-instagram"></i>
            <i class="fa-brands fa-square-pinterest"></i>
            <i class="fa-brands fa-square-youtube"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss">
.container-footer{
  background-color: #1a1a1a;
  height: 80px;
}

.container-footer .text-footer{
  max-width: 1030px;
  height: 80px;
  margin: auto;
  display: flex;
  justify-content: space-between;
}

.text-footer .boolando{
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.text-footer .menu a{
  font-size: 11px;
}

.text-footer .social{
  display: flex;
  align-items: center;
}

.text-footer .trovaci{
  color: white;
  display: flex;
  flex-direction: column;
}

.social h4{
  font-size: 11px;
  padding-bottom: 6px;
}

.social .fa-brands{
  padding-right: 5px;
}
</style>