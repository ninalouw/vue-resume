<template>
  <div class="container">
    <h1 class="text-center">{{title}}</h1>

    <div class="row">
      <div v-for="item in data"
           :key="item.id"
           class="block col-lg-4 col-md-6 col-sm-12 col-xs-12">
        <div class="card" :width="item.width">
          <img class="card-img-top img-fluid" :src="getImgUrl(item.img)" alt="Card image cap">
          <div class="card-block">
            <h3 class="card-title">{{item.title}}</h3>
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
      return images(`./${name}.jpg`);
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
   width: 100%
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
@media (max-width: 568px)
  .card
  .card-mobile
    width: 95%
    margin: 10px

    .card-img-top
      width: 100%
      height: 200px
    .card-text
      font-size: 0.8rem
h3
  font-size: 1.7rem
p
  font-size: 0.8rem
.btn
  font-size: 0.8rem
</style>
