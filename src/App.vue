<template>
  <div id="app">
    <img class="logo" src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
#app {
  font-family: 'Anonymous Pro', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50; */
  margin-top: 30px;
}
.logo {
    margin-left:60px;
    margin-bottom:60px;
    width: 100px;
    height: 100px;
}
</style>
