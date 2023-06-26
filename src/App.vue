<template>
  <nav>
    <router-link to="/">Home</router-link> 
    
  </nav>
  <router-view/>

<footer>
  Copyright @ 2023
</footer>  
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
  padding: 20px;
  background-color: black;
  align-items: start;
}

nav a {
  font-weight: bold;
  color: orangered;
}

nav a.router-link-exact-active {
  color: #b94242;
}

footer{
  padding: 20px;
  background-color: black;
  color: orangered;
}
</style>
