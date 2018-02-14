<template>
  <div class="container">
    <h1 class="text-center">{{ title }}</h1>
    <div class="row block-section">
      <div class="block col-lg-6 col-md-6 col-sm-6 col-xs-12">
        <h2>{{ subTitle1 }}</h2>
        <div class="svgs">
          <i class="devicon-trello-plain colored"></i>
        </div>
        <p>{{ para1 }}</p>
      </div>
      <div class="block col-lg-6 col-md-6 col-sm-6 col-xs-12">
        <h2>{{ subTitle2 }}</h2>
        <div class="svgs">
          <i class="devicon-photoshop-plain colored"></i>
          <i class="devicon-illustrator-plain colored"></i>
        </div>
        <p>{{ para2 }}</p>
      </div>
    </div>
    <div class="row">
      <div class="block col-lg-6 col-md-6 col-sm-6 col-xs-12">
        <h2>{{ subTitle3 }}</h2>
        <div class="svgs">
          <i class="devicon-html5-plain-wordmark colored"></i>
          <i class="devicon-css3-plain-wordmark colored"></i>
          <i class="devicon-sass-original colored"></i>
          <i class="devicon-bootstrap-plain-wordmark colored"></i>
          <i class="devicon-javascript-plain colored"></i>
          <i class="devicon-jquery-plain-wordmark colored"></i>
          <i class="devicon-angularjs-plain colored"></i>
          <i class="devicon-react-original-wordmark colored"></i>
          <i class="devicon-vuejs-plain-wordmark colored"></i>
          <i class="devicon-webpack-plain colored"></i>
          <i class="devicon-babel-plain colored"></i>
          <i class="devicon-mocha-plain colored"></i>
          <i class="devicon-jasmine-plain-wordmark colored"></i>
          <i class="devicon-grunt-line-wordmark colored"></i>
          <i class="devicon-gulp-plain colored"></i>
        </div>
        <p>{{ para3 }}</p>
      </div>
      <div class="block col-lg-6 col-md-6 col-sm-6 col-xs-12">
        <h2>{{ subTitle4 }}</h2>
        <div class="svgs">
          <i class="devicon-ruby-plain colored"></i>
          <i class="devicon-rails-plain-wordmark colored"></i>
          <i class="devicon-php-plain colored"></i>
          <i class="devicon-laravel-plain-wordmark colored"></i>
          <i class="devicon-nodejs-plain colored"></i>
          <i class="devicon-express-original-wordmark colored"></i>
          <i class="devicon-heroku-plain-wordmark colored"></i>
          <i class="devicon-amazonwebservices-plain-wordmark colored"></i>
          <i class="devicon-mysql-plain-wordmark colored"></i>
          <i class="devicon-nginx-plain-wordmark colored"></i>
          <i class="devicon-postgresql-plain-wordmark colored"></i>
          <i class="devicon-mongodb-plain-wordmark colored"></i>
          <i class="devicon-cucumber-plain colored"></i>
          <i class="devicon-redis-plain-wordmark colored"></i>
          <i class="devicon-git-plain colored"></i>
        </div>
        <p>{{ para4 }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import Data from '../data/data.json';

export default {
  name: 'Skills',
  data() {
    return {
      title: Data.Skills.title,
      subTitle1: Data.Skills.subTitle1,
      subTitle2: Data.Skills.subTitle2,
      subTitle3: Data.Skills.subTitle3,
      subTitle4: Data.Skills.subTitle4,
      para1: Data.Skills.para1,
      para2: Data.Skills.para2,
      para3: Data.Skills.para3,
      para4: Data.Skills.para4,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
h1, h2
  font-weight: bold
  font-family: 'Playfair Display', serif
.block-section
  margin-top: 60px
.block
  display: flex
  flex-direction: column
  align-content: center
  i
    font-size: 6rem
    margin: 10px 10px 20px 0px
    padding: 10px
  .svgs
    margin-top: 30px
    margin-bottom: 30px

</style>
