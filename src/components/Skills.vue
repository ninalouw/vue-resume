<template>
  <div class="container" id="skills">
    <h1 class="text-center">{{ title }}</h1>

    <div class="row block-section">
      <div v-for="item in data"
           :key="item.id"
           class="block col-lg-6 col-md-6 col-sm-12 col-xs-12">
        <h2>{{ item.title }}</h2>
        <div class="svgs">
          <i :class="item.icons"></i>
        </div>
        <p>{{ item.para }}</p>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 buttons">
        <a href="https://github.com/ninalouw" class="btn btn-primary">View Github</a>
        <a :href="getPdfUrl('Nina_Louw_Resume')"
            target="_blank" class="btn btn-secondary">Download Resume</a>
        <a href="mailto:ninalouw@mac.com" class="btn btn-tertiary">Contact Me</a>
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
      title: 'Skills & Approach',
      data: Data.Skills,
    };
  },
  methods: {
    getPdfUrl(name) {
      const pdf = require.context('../assets/', false, /\.pdf$/);
      return pdf(`./${name}.pdf`);
    },
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
  display: flex
  align-items: left
  justify-content: space-evenly
  .btn
    padding: 10px 20px 10px 20px
    margin-right: 5px
    margin-top: 10px
    border-radius: 0%
    &:hover
      cursor: pointer
  .btn-primary
    background-color: #7EC1CC
    border: 1px solid #65CFE1
    color: white
    &:hover
  .btn-secondary
    background-color: #FFFAD0
    border: 1px solid #FDF296
    color: black
    &:hover
      color: white
      background-color: #FBE73F
  .btn-tertiary
    color: white
    background-color: #25B6CD
    background-color: #FFC8D9
    border: 1px solid #FDB0D5
    &:hover
      background-color: #FC4099
@media (max-width: 568px)
  .buttons
    flex-direction: column
    align-items: center
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
    i
      font-size: 2rem
    .svgs
      margin: 15px
</style>
