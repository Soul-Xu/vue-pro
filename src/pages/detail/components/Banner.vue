<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img"
        src="https://imgs.qunarzz.com/sight/p0/1912/78/78fdc5a98b55aaefa3.water.jpg_710x360_cd2c6599.jpg">
      <div class="banner-info">
        <div class="banner-title">
          香港迪士尼乐园
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe63d;</span>
          399
        </div>
      </div>
    </div>
    <common-gallary @close="handleGallayClose" :imgs="imgs" v-show="showGallary"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['https://imgs.qunarzz.com/sight/p0/1606/64/645bc9ccffa23ef90.water.jpg_990x390_0cfe520c.jpg',
        'https://imgs.qunarzz.com/sight/p0/201405/27/713c21a94e2ec1832df29096d13522dc.jpg_990x390_91feab09.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallayClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
  // 防止页面抖动
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: .2rem
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .12rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
