<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img src="//img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_600x330_2285872d.jpg"
      class="banner-img">
      <div class="banner-info">
        <div class="banner-title">东方明珠(AAAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          30
          </div>
      </div>
    </div>
    <common-gallary
    :imgs="imgs"
    v-show="showGallary"
    @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_r_800x800_4228e25a.jpg', 'http://img1.qunarzz.com/sight/p0/1411/b2/ffd511789081a81d84379ce6891ae623.water.jpg_r_800x800_47a275a2.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
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
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        font-size .32rem
        padding 0 .2rem
        flex 1
      .banner-number
        height .32rem
        line-height .32rem
        margin-top .14rem
        padding 0 .4rem
        border-radius .2rem
        font-size .24rem
        background rgba(0, 0, 0, .8)
        .banner-icon
          font-size .24rem
</style>
