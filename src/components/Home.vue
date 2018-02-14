<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12 hero-text">
        <h1>{{ title }}</h1>
        <p> {{ intro }}</p>
        <button class="btn btn-outline-primary">Email</button>
        <button class="btn btn-outline-primary">Github</button>
        <button class="btn btn-outline-primary">LinkedIn</button>
      </div>
      <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12 hero-video">
        <canvas></canvas>
      </div>
    </div>
    <app-about></app-about>
  </div>
</template>

<script>
import Data from '../data/data.json';
import About from './About.vue';

export default {
  name: 'Home',
  data() {
    return {
      title: Data.Home.title,
      intro: Data.Home.intro,
    };
  },
  components: {
    appAbout: About,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  margin-top:60px;
  margin-bottom:60px;
}
h1 {
font-weight: bold;
font-family: 'Playfair Display', serif;
font-size: 5rem;
}
p {
  max-width: 450px;
  font-size: 2rem;
  font-family: 'Anonymous Pro', monospace;
}
canvas {
  background-color: #FFC8D9;
  width: 480px;
  height: 430px;
}
.btn-outline-primary {
  border: solid 1px #FFC8D9;
  padding: 8px 16px 8px 16px;
  margin-right:5px;
  margin-top:10px;
  border-radius: 0%;
}
button .btn-outline-primary :hover{
  cursor: pointer;
  background-color: #FFC8D9;
  color: #fff;
}
</style>
