<template>
  <nav class="navbar navbar-toggleable-md navbar-light bg-faded">
    <button class="navbar-toggler navbar-toggler-right" type="button"
            data-toggle="collapse"
            data-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
     <a class="navbar-brand" href="/#/">
      <img class="logo" src="../assets/logo.png" width="30" height="30" alt="logo">
    </a>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <a class="nav-link" @click.prevent="scrollToSection('about')" href="/#/">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" @click.prevent="scrollToSection('skills')" href="/#/">Skills</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/#/work">Work</a>
        </li>
        <li class="nav-item">
          <a class="btn btn-primary" href="mailto:ninalouw@mac.com">Contact Me</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>

export default {
  name: 'Header',
  updated() {
    const elem = this.$el;
    elem.scrollTop = elem.clientHeight;
  },
  methods: {
    scrollToSection(id) {
      const element = document.getElementById(`${id}`);
      element.scrollIntoView();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
.bg-faded
    background-color: #fff

.navbar-light .navbar-nav .nav-link
    color: rgba(0,0,0,.9)
    padding-left: 5rem
    padding-right: 5rem
    font-size: 1.2rem

.logo
  margin-left: 60px
  margin-bottom: 20px
  width: 135px
  height: 135px

.btn
  padding: 10px 20px 10px 20px
  margin-right: 5px
  margin-top: 2px
  margin-left: 4rem;
  border-radius: 0%
  &:hover
    cursor: pointer
.btn-primary
  background-color: #FFC8D9
  border: 1px solid #FFC8D9
  &:hover
    background-color: #FC4099
</style>
