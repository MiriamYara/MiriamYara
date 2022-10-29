<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      <router-link to="/Ejemplor">Ejemplor</router-link>
      <router-link to="/Vif">Ejemplo Vif</router-link>
      <router-link to="/Vfor">Ejemplo Vfor</router-link>
      <router-link to="/Vmodel">Ejemplo model</router-link>
      <router-link to="/Von">Ejemplo Von</router-link>

      
    </nav>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
