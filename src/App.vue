<template>
  <div id="app">
    <app-header></app-header>
    <router-view/>
    <app-footer></app-footer>
  </div>
</template>

<script>

import Header from './components/Header';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    appHeader: Header,
    appFooter: Footer,
  },
};
</script>

<style lang="sass">
#app
  font-family: 'Anonymous Pro', monospace
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  /* text-align: center; */
  /* color: #2c3e50; */
  margin-top: 30px

.container
  margin-top: 60px
  margin-bottom: 60px

</style>
