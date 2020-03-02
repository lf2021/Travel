<template>
  <div class="header">
    城市选择
    <router-link to='/'>
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl'
  .header
    overflow hidden
    height $headerHeight
    line-height $headerHeight
    background $bgColor
    color #fff
    text-align center
    font-size .32rem
    position relative
    .header-back
      position absolute
      left 0
      top 0
      width .64rem
      text-align center
      font-size .4rem
      color #fff
</style>
