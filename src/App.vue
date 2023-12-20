<template>
  <nav>
    <img src="./icon.png" alt="an image of the logo of our company CollegeSeminar">
    <router-link :to="{ name: 'home' }">Home</router-link> |
    <router-link :to="{ name: 'Seminars' }">Seminars</router-link> |
    <router-link :to="{ name: 'Contact' }">Contact</router-link>
  </nav>
  <router-view/>
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

nav img {
  /* float:right;  */
  position: relative;
  top: 0.5em;
  right: 0.5em;
  width: 2em; 
  height:2em; 
  border-radius: 50%;
  opacity: 0.8;
  
}
</style>
