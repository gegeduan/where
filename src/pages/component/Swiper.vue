<template>
    <div class='wrapper'>
        <swiper :options="swiperOptions" v-if='showSwiper'>
            <swiper-slide v-for='item of list' :key='item.id'>
                <img :src='item.imgUrl' class='swiper-img'>
            </swiper-slide>
             <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
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
