<template>
  <footer class="footer">
    <span>Get in contact with me at </span>
    <span>
      <i class="fas fa-1x fa-envelope"></i>
      <a href="mailto:ninalouw@mac.com">ninalouw@mac.com</a>
    </span>
    <span>
      <i class="fab fa-1x fa-linkedin"></i>
      <a href="https://www.linkedin.com/in/ninamaelouw/">LinkedIn</a>
    </span>
    <span>DM me on Twitter</span>
    <span>
      <i class="fab fa-1x fa-twitter"></i>
      <a href="https://twitter.com/ninamaelouw">@ninamaelouw</a>
    </span>
  </footer>
</template>

<script>

export default {
  name: 'Footer',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@media (max-width: 768px)
  .footer
    flex-direction: column
    align-items: left

p, a
  font-size: 1rem
.footer
  display: flex
  justify-content: space-evenly
  align-items: center
  background-color: #FFFAD0
  padding: 60px
  margin-top: 30px
  span
    a
      color: black
      &:hover
        cursor: pointer
        color: #F8B91C
    i
      &:hover
        cursor: pointer
        color: #F8B91
</style>
