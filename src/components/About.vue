<template>
  <div class="container">
    <h1 class="text-center">{{ title }}</h1>
    <div class="row block-section">
      <div class="block col-lg-5 col-md-5 col-sm-5 col-xs-12">
        <img class="img-responsive" src="../assets/book.svg">
        <h2>{{ subTitle1 }}</h2>
        <p>{{ para1 }}</p>
      </div>
      <div class="block block-left col-lg-5 col-md-5 col-sm-5 col-xs-12">
        <img class="img-responsive" src="../assets/laptop.svg">
        <h2>{{ subTitle2 }}</h2>
        <p>{{ para2 }}</p>
      </div>
    </div>
    <div class="row">
      <div class="block col-lg-5 col-md-5 col-sm-5 col-xs-12">
        <img class="img-responsive" src="../assets/dev.svg">
        <h2>{{ subTitle3 }}</h2>
        <p>{{ para3 }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import Data from '../data/data.json';
import Book from '../assets/book.svg';
import Dev from '../assets/dev.svg';
import Laptop from '../assets/laptop.svg';

export default {
  name: 'About',
  data() {
    return {
      title: Data.About.title,
      subTitle1: Data.About.subTitle1,
      subTitle2: Data.About.subTitle2,
      subTitle3: Data.About.subTitle3,
      para1: Data.About.para1,
      para2: Data.About.para2,
      para3: Data.About.para3,
      image1: Book,
      image2: Laptop,
      image3: Dev,
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
</style>
