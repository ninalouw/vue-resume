<template>
  <div class="container">
    <h1>{{title}}</h1>
    <div class="row">
      <div v-for="value in data" class="col-lg-4 col-md-4 col-sm-4 col-xs-12">
        <div class="card" style="width: 20rem;">
        <img class="card-img-top" src="..." alt="Card image cap">
        <div class="card-block">
          <h4 class="card-title">{{value}}</h4>
          <p class="card-text">{{value}}</p>
          <a href="#" class="btn btn-primary">View Site</a>
          <a href="#" class="btn btn-primary">Source code</a>
        </div>
        </div>
      </div>
      <!-- <div class="col-lg-4 col-md-4 col-sm-4 col-xs-12">
        <div class="card" style="width: 20rem;">
        <img class="card-img-top" src="..." alt="Card image cap">
        <div class="card-block">
          <h4 class="card-title">{{subTitle2}}</h4>
          <p class="card-text">{{para2}}</p>
          <a href="#" class="btn btn-primary">View Site</a>
          <a href="#" class="btn btn-primary">Source code</a>
        </div>
        </div>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-4 col-xs-12">
        <div class="card" style="width: 20rem;">
        <img class="card-img-top" src="..." alt="Card image cap">
        <div class="card-block">
          <h4 class="card-title">{{subTitle3}}</h4>
          <p class="card-text">{{para3}}</p>
          <a href="#" class="btn btn-primary">View Site</a>
          <a href="#" class="btn btn-primary">Source code</a>
        </div>
        </div>
      </div> -->
    </div>
  </div>
</template>

<script>
import Data from '../data/data.json';

export default {
  name: 'Work',
  data() {
    return {
      title: Data.Work.title,
      data : Data.Work,
      // subTitle1: Data.Work.subTitle1,
      // subTitle2: Data.Work.subTitle2,
      // subTitle3: Data.Work.subTitle3,
      // subTitle4: Data.Work.subTitle4,
      // subTitle5: Data.Work.subTitle5,
      // subTitle6: Data.Work.subTitle6,
      // para1: Data.Work.para1,
      // para2: Data.Work.para2,
      // para3: Data.Work.para3,
      // para4: Data.Work.para4,
      // para5: Data.Work.para5,
      // para6: Data.Work.para6,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
h1, h2
  font-weight: bold
  font-family: 'Playfair Display', serif
</style>
