<template lang="pug">
#app
  b-navbar(toggleable='')
    b-nav-toggle(target='nav_collapse')
      a.navbar-brand(to='/')
        span スキル申告
      b-collapse#nav_collapse(isnav='')
        b-nav(isnavbar='')
          b-nav-item Support
          b-nav-item Docs
          b-nav-item Contact Us
          .navbar-nav
            router-link.nav-item.nav-link(to="/") 回答状況一覧


  router-view
</template>

<script>

export default {
  name: 'app'
}

</script>

<style lang="stylus">
#app
  font-family "游ゴシック", YuGothic, "ヒラギノ角ゴ Pro", "Hiragino Kaku Gothic Pro", "メイリオ", "Meiryo", sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale

nav
  margin-bottom 32px
  // background-color lightgray

</style>
