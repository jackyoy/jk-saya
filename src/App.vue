<template>
  <div id="app">
    <div class="logo">
      <img src="../src/assets/logo.png" alt="logo" title="JK-World">
    </div>
    <div id="nav" class="d-flex justify-content-center">
      <b-nav>
        <b-nav-item>
          <router-link to="/">首頁</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="/Calculation">計算</router-link>
        </b-nav-item>
      </b-nav>
    </div>
    <router-view/>
  </div>
</template>



<style scoped lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 3px;
  text-align: center;
  a {
    font-weight: bold;
    color: #2c3e50;
    padding: 10px;
    :hover {
      color: darkgoldenrod;
    }
    &.router-link-exact-active {
      color: brown;
    }
  }
}
img {
  max-width: 100%;
  height: auto;
}
.logo {
  border-bottom: 5px dotted #a9a9a9;
  text-align: left;
}
</style>

