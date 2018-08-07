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
        <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12 video-cont">
            <video class="hero-video" :src="getImgUrl(video)"
                   type="video/mp4" autoplay controls></video>
        </div>
      </div>
      <app-about></app-about>
      <app-skills></app-skills>
    </div>
  </div>
</template>

<script>
import Data from '../data/data.json';
import About from './About';
import Skills from './Skills';

export default {
  name: 'Home',
  data() {
    return {
      title: Data.Home.title,
      intro: Data.Home.intro,
      video: Data.Home.video,
    };
  },
  components: {
    appAbout: About,
    appSkills: Skills,
  },
  methods: {
    getImgUrl(name) {
      const images = require.context('../assets/', false, /\.mp4$/);
      return images(`./${name}.mp4`);
    },
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
.video-cont
  padding-top: 70px
.hero-video
  width: 100%
  height: 328px
  -webkit-box-shadow: 0 2px 6px 0 rgba(0,0,0,0.17);
  -moz-box-shadow: 0 2px 6px 0 rgba(0,0,0,0.17);
  box-shadow: 0 2px 6px 0 rgba(0,0,0,0.17);
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

@media (max-width: 568px)
  h1
    font-size: 3.8rem

  h2
    font-size: 1.3rem

  h3
    font-size: 1rem

  h4
    font-size: 1rem
  p
    font-size: 0.9rem
</style>
