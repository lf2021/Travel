<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">上海</div>
          </div>
          <div class="button-wrapper">
            <div class="button">三亚 </div>
          </div>
          <div class="button-wrapper">
            <div class="button">香港</div>
          </div>
          <div class="button-wrapper">
            <div class="button">杭州</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">B</div>
        <div class="item-list">
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
          <div class="item border-bottom">巴中</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .border-topbottom
    &:before
      border-color #ccc
    &:after
      border-color #ccc
  .border-bottom
    &:before
      border-color #ccc
  .list
    overflow hidden
    position absolute
    left 0
    top 1.58rem
    right 0
    bottom 0
    .title
      line-height .54rem
      background-color #eee
      padding-left .2rem
      color #666
      font-size .26rem
    .button-list
      padding .1rem
      padding .1rem .6rem .1rem .1rem
      overflow hidden
      .button-wrapper
        float left
        width 33.3%
        .button
          text-align center
          padding .1rem 0
          margin .1rem
          border .02rem solid #ccc
          border-radius .06rem
    .item-list
      .item
        line-height .54rem
        padding-left .2rem
</style>
