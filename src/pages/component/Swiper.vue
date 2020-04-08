<template>
    <div class='wrapper'>
        <swiper :options="swiperOptions">
            <swiper-slide v-for='item of swiperList' :key='item.id'>
                <img :src='item.imgUrl' class='swiper-img'>
            </swiper-slide>
             <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '001',
          imgUrl: '//img1.qunarzz.com/sight/p0/1811/2f/2f31b8d1536a2564a3.img.jpg_600x330_98e22c1e.jpg'
        },
        {
          id: '002',
          imgUrl: '//img1.qunarzz.com/sight/p0/1511/49/499c8f4ce3968f9c90.img.jpg_600x330_ce81f941.jpg'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background:#fff
.wrapper
    overflow:hidden
    width:100%
    height:0
    padding-bottom:36.7%
    background:#eee;
    .swiper-img
        width:100%
</style>
