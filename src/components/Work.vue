<template>
  <div class="container">
    <h1 class="text-center">{{title}}</h1>

    <div class="row">
      <div v-for="item in data"
           :key="item.id"
           class="block col-lg-4 col-md-4 col-sm-4 col-xs-12">
        <div class="card" style="width: 20rem;">
          <img class="card-img-top" src="" alt="Card image cap">
          <div class="card-block">
            <h4 class="card-title">{{item.title}}</h4>
            <p class="card-text">{{item.para}}</p>
            <a :href="item.url" class="btn btn-primary">View Site</a>
            <a :href="item.source_code" class="btn btn-primary">Source code</a>
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
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
h1, h2
  font-weight: bold
  font-family: 'Playfair Display', serif
</style>
