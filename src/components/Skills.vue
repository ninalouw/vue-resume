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
    <div class="row buttons">
      <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12">
        <button href="https://github.com/ninalouw" class="btn btn-primary">View Github</button>
        <button class="btn btn-secondary">Download Resume</button>
        <button href="mailto:ninalouw@mac.com" class="btn btn-tertiary">Contact Me</button>
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
    font-size: 4rem
    // margin: 5px 5px 10px 0px
    padding-top: 2px
    color: #F7E866
    &:before
      margin: 10px
  .svgs
    margin-top: 30px
    margin-bottom: 30px

.buttons
  margin-top: 30px
  margin-bottom: 30px
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
  .btn-secondary
    background-color: #FFFAD0
    border: 1px solid #FDF296
    color: black
    margin-left: 95px
  .btn-tertiary
    background-color: #7EC1CC
    border: 1px solid #65CFE1
    margin-left: 95px

</style>
