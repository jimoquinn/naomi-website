<template>
  <section class="alert-banner">
    <div class="alert">
    {{$page.frontmatter.alert}}
    </div>
    <div class="alert-button-container">
      <router-link :to="$page.frontmatter.alert_link || '/download/'" class="alert-button slide">Download it Now! ➜</router-link>
    </div>
  </section>
</template>

<style lang="stylus">
.alert-banner
  background-color red
  font-size 2rem
  padding 0.5rem
  color white
  text-align center
  display flex
  justify-content center
  align-items center
  .alert
    padding-right 1rem
  .alert-button-container
    text-align center
  .alert-button
    display inline-block
    font-family 'Open Sans', sans-serif
    font-size 1rem
    font-weight bold
    color white
    padding 0.8rem 1.6rem
    border-radius 4px
    transition background-color .1s ease
    box-sizing border-box
    border 2px solid white
    &:hover
      background-color white
      color #1397d5
  @media (max-width 479px)
    &
      flex-direction column
    .alert
      padding-right 0
    .alert-button-container
      padding-top 0.8rem
</style>
