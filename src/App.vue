<template>
  <nav>
    <router-link to="/">Dars jadvali</router-link> 
    <router-link to="/courses">Kurslar</router-link>
     <router-link to="/about">Yangiliklar</router-link>
  </nav>
  <router-view/>

</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #414f5d;
  /* min-width: 360px; */
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #414f5d;
  padding: 10px;
  background: #fff;
  border-radius: 5px;
  border:1px solid #414f5d;
  text-decoration: none;
  margin: 10px
}



nav a.router-link-exact-active {
  background: #414f5d;
  color:#fff;
}

/*  */
</style>
