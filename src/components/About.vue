<template>
  <div class="container" id="about">
    <h1 class="text-center">{{ title }}</h1>
    <div class="row block-section">
      <div v-for="item in data"
            class="block col-lg-6 col-md-6 col-sm-12 col-xs-12"
            :key="item.id"
            >
        <img class="img-responsive" :src="getImgUrl(item.img)">
        <h2>{{ item.title }}</h2>
        <p>{{ item.para }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import Data from '../data/data.json';

export default {
  name: 'About',
  data() {
    return {
      data: Data.About,
      title: 'About',
    };
  },
  methods: {
    getImgUrl(name) {
      const images = require.context('../assets/', false, /\.svg$/);
      return images(`./${name}.svg`);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
.container
  margin-top: 140px
h1, h2
  font-weight: bold
  font-family: 'Playfair Display', serif
.block-section
  margin-top: 60px
.block-left
  margin-left: 60px
  margin-top: 60px
.block
  display: flex
  flex-direction: column
  align-content: center
  img
    width: 100px
    align-self: center
@media (max-width: 568px)
  h1
    font-size: 2rem

  h2
    font-size: 1.3rem

  h3
    font-size: 1.1rem

  h4
    font-size: 1rem
  p
    font-size: 0.7rem
  .block
    img
      width: 80px
</style>
