<template>
  <div class="app">
    <div class="nav-container">
      <div class="nav-content">
        <router-link to="/">
          <i class="bx bx-home bx-sm"></i>
        </router-link>
         <router-link to="/cesta">
          <i class="bx bx-basket bx-sm"></i>
        </router-link>
        <router-link to="/favoritos">
          <i class="bx bx-heart bx-sm"></i>
        </router-link>
        <router-link to="/historial">
          <i class="bx bx-rotate-right bx-sm"></i>
        </router-link>
      </div>
    </div>
    <router-view />
  </div>
</template>

<style lang="less">
.nav-container {
  width: 100%;
  position: fixed;//poner encima de los elementos
  bottom: 0;//pegar abajo el elemento
  .nav-content {
    padding: 20px;
    display: flex;
    justify-content: space-between;//abir objetos horizontalmente
    a{
      color:#292929;
      &.router-link-exact-active {
        color: rgba(70, 208, 218);
      }
    }
  }
}

#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color:gray;
}

* {
  margin: 0;
  padding: 0%;
}
</style>
