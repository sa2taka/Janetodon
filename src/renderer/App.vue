<template>
  <div id="app">
    <nav class="navbar main-nav" role="navigation" aria-label="main navigation">
      <div class="navbar-menu">
        <div class="navbar-end">
        </div>
      </div>
    </nav>

    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'janetodon'
}
</script>

<style lang="sass">
html body
  background-color: $main-background!important
  color: white
  height: 100vh

  &::-webkit-scrollbar
    display: none

a
  color: $a-color!important
  background-color: $main-background!important
  &:hover
    background-color: rgb(26, 29, 36)!important
    color: $a-color!important
.main-nav
  width: 100%
  height: 60px
  position: fixed
  z-index: 1000
  background-color: $main-background
  color: white

.fa-icon
  width: auto
  height: 1em

  /* You would have to include the following two lines to make this work in Safari */
  max-width: 100%
  max-height: 100%

  margin: 2px

</style>
