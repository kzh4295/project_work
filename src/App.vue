<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/personal">업무 보고서_개인별</router-link> |
    <router-link to="/team">업무 보고서_팀별</router-link> |
    <router-link to="/part">업무 보고서_파트별</router-link> 
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
</style>
