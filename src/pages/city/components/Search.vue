<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .search
    height .72rem
    padding 0 .1rem
    background $bgColor
    .search-input
      height .62rem
      line-height .62rem
      width 100%
      color #666
      text-align center
      box-sizing border-box
      padding 0 .1rem
      border-radius .06rem
</style>
