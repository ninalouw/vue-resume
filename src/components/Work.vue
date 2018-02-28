<template>
  <div class="container">
    <h1 class="text-center">{{title}}</h1>

    <div class="row">
      <div v-for="item in data"
           :key="item.id"
           class="block col-lg-4 col-md-6 col-sm-12 col-xs-12">
        <div class="card" :width="item.width">
          <img class="card-img-top" :src="getImgUrl(item.img)" alt="Card image cap">
           <!-- <video class="card-img-top hero-video" :src="getVideoUrl(item.img)" type="video/mov"  width="580" height="328" autoplay controls></video> -->
          <div class="card-block">
            <h4 class="card-title">{{item.title}}</h4>
            <p class="card-text">{{item.para}}</p>
            <a :href="item.url" class="btn btn-primary">View Site</a>
            <a :href="item.source_code" class="btn btn-tertiary">Source code</a>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import Data from '../data/data.json';

export default {
  name: 'Work',
  data() {
    return {
      title: 'Work',
      data: Data.Work,
    };
  },
  methods: {
    getImgUrl(name) {
      const images = require.context('../assets/', false, /\.jpg$/);
      return images('./' + name + '.jpg');
    },
    getVideoUrl(name) {
      const images = require.context('../assets/', false, /\.mp4$/);
      return images('./' + name + '.mp4');
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
h1, h2
  font-weight: bold
  font-family: 'Playfair Display', serif

@mixin soft-shadow
  -webkit-box-shadow: 0 2px 6px 0 rgba(0,0,0,0.17)
  -moz-box-shadow: 0 2px 6px 0 rgba(0,0,0,0.17)
  box-shadow: 0 2px 6px 0 rgba(0,0,0,0.17)
.row
  margin-top: 60px
  margin-bottom: 60px
.card
  @include soft-shadow
  border: none
  margin-top: 15px
  margin-bottom: 15px
  .card-img-top
    height: 400px
  .hero-video
    width: 580px
    height: 328px
  .btn
    padding: 10px 20px 10px 20px
    margin-right: 5px
    margin-top: 10px
    border-radius: 0%
    &:hover
      cursor: pointer
  .btn-primary
    background-color: #FFC8D9
    border: 1px solid #FDB0D5
    &:hover
      background-color: #FC4099
  .btn-tertiary
    color: white
    background-color: #7EC1CC
    border: 1px solid #65CFE1
    &:hover
      color: white
      background-color: #25B6CD
</style>
