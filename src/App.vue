<template>
  <nav>
    <router-link :to="{name: 'home'}">Todos</router-link>
    <router-link :to="{name: 'categories'}">Categories</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width :80%;
  margin: 0 auto;
}

nav {
  padding: 30px;
}

nav a {
  
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 8px 12px;
}

nav a.router-link-exact-active {
  color: white;
  background-color: #42b983;
}
</style>
