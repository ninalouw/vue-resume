<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12 hero-text">
          <h1>{{ title }}</h1>
          <p> {{ intro }}</p>
            <div class="contact">
            <span>
              <i class="fas fa-2x fa-envelope"></i>
              <a href="mailto:ninalouw@mac.com">Email</a>
            </span>
            <span>
              <i class="fab fa-2x fa-github"></i>
              <a href="https://github.com/ninalouw">Github</a>
            </span>
            <span>
              <i class="fab fa-2x fa-linkedin"></i>
              <a href="https://www.linkedin.com/in/ninamaelouw/">LinkedIn</a>
            </span>
          </div>
        </div>
        <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12 hero-video">
          <canvas></canvas>
        </div>
      </div>
      <app-about></app-about>
      <app-skills></app-skills>
    </div>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Data from '../data/data.json';
import About from './About';
import Skills from './Skills';
import Footer from './Footer';

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
    appSkills: Skills,
    appFooter: Footer,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
h1
  font-weight: bold
  font-family: 'Playfair Display', serif
  font-size: 5rem

p
  max-width: 450px
  margin-top: 30px
  margin-bottom: 30px
  font-size: 1.2rem
  font-family: 'Anonymous Pro', monospace

canvas
  background-color: #FFC8D9
  width: 480px
  height: 430px
.contact
  display: flex
  justify-content: space-between
  align-items: center
  margin-top: 15px
  span
    a
      color: black
      &:hover
        cursor: pointer
        color: #FFC8D9
    i
      color: #FFC8D9
      &:hover
        cursor: pointer
        color: #FDB0D5
</style>
