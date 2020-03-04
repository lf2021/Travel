<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg">
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-number">
          <span class="iconfont">&#xe692;</span>
          {{this.galleryImgs.length}}
        </div>
      </div>
    </div>
    <fade-animation>
      <common-gallery
        @close="handleGalleryClose"
        :imgs="galleryImgs"
        v-show="showGallery"
      >
      </common-gallery>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
import FadeAnimation from 'common/Fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    galleryImgs: Array
  },
  data () {
    return {
      showGallery: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1510/8e/8eea8eb6f41698290.img.jpg_r_800x800_83a5fe3a.jpg', 'http://img1.qunarzz.com/sight/p0/1510/ca/ca60a080020329ef90.img.jpg_350x240_9ff2208e.jpg']
    }
  },
  components: {
    CommonGallery,
    FadeAnimation
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      color #fff
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        margin .14rem
        padding 0 .3rem
        height .32rem
        line-height .32rem
        border-radius .2rem
        background rgba(0, 0, 0, .8)
        font-size .24rems
</style>
