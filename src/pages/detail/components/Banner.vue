<template>
    <div class='wrapper'>
        <div class="banner" @click='handleBannerClick'>
                <img class='banner-img' src='//img1.qunarzz.com/sight/p0/201301/08/04d0fc5bc44b81d693835fbb.jpg_600x330_6a566e24.jpg'>
                <div class='banner-info'>
                    <div class='info-title'>上海世纪公园</div>
                    <div class='info-num'>
                        <span class='iconfont number-icont'>&#xe729;</span>
                        39
                    </div>
                </div>
        </div>
        <common-gallery
         :imgs='imgs'
         v-show='showGallery'
         @close='handleGalleryClose'></common-gallery>
    </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallery
  },
  data () {
    return {
      showGallery: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201301/08/39226d29be846f9793835fbb.jpg_350x240_f9877046.jpg', 'http://img1.qunarzz.com/sight/p0/201301/08/342f038bfea5e31d93835fbb.jpg_350x240_1564cba6.jpg']
    }
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

<style  lang='stylus' scoped>
.banner
  position:relative
  overflow:hidden
  height:0
  padding-bottom:55%
  color:#fff
  .banner-img
    width:100%
  .banner-info
    display:flex
    position:absolute
    left:0
    right:0
    bottom:0
    background-image:linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    .info-title
      flex:1
      font-size:.32rem
      padding:0 .2rem
    .info-num
      height 0.42rem
      line-height:.42rem
      font-size:.24rem
      padding:0 .2rem
      border-radius:.2rem
      background:rgba(0,0,0,0.8)
      .number-icont
        font-size:.24rem

</style>
