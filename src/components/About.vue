<template>
  <div class="container">
    <h1 class="text-center">{{ title }}</h1>
    <div class="row">
      <div class="col-lg-4 col-md-4 col-sm-4 col-xs-6">
        <h2>{{ subTitle1 }}</h2>
        <p>{{ para1 }}</p>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-4 col-xs-6">
        <h2>{{ subTitle2 }}</h2>
        <p>{{ para2 }}</p>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-4 col-xs-6">
        <h2>{{ subTitle3 }}</h2>
        <p>{{ para3 }}</p>
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
      title: Data.About.title,
      subTitle1: Data.About.subTitle1,
      subTitle2: Data.About.subTitle2,
      subTitle3: Data.About.subTitle3,
      para1: Data.About.para1,
      para2: Data.About.para2,
      para3: Data.About.para3,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
font-weight: bold;
font-family: 'Playfair Display', serif;
}

</style>
