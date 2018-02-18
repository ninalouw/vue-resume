<template>
  <div class="container">
    <h1 class="text-center">{{ title }}</h1>
    <div class="row block-section">
      <div v-for="item in data"
            class="block col-lg-6 col-md-6 col-sm-6 col-xs-12"
            :key="item.id"
            >
        <img class="img-responsive" :src="item.img">
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
      title: 'My Journey',
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
