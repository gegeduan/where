<template>
  <div class="gallery" @click='handleGalleryClick'>
       <div class='img-wrapper'>
            <swiper :options="swiperOptions">
                <swiper-slide v-for='(item, index) of imgs' :key='index'>
                    <img class='gallery-img' :src='item'>
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
       </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallery',
  props: {
    imgs: Array,
    default () {
      return []
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observer: true,
        observeParents: true
      }
    }
  },
  methods: {
    handleGalleryClick () {
      this.$emit('close')
    }
  }
}
</script>

<style  lang='stylus' scoped>
.gallery >>> .swiper-container
   overflow:inherit
.gallery
  display:flex
  flex-direction:column
  justify-content:center
  position:fixed
  top:0
  left:0
  right:0
  bottom:0
  background:#000
  .img-wrapper
    height:0
    padding-bottom:70%
    .gallery-img
      width:100%
    .swiper-pagination
      position:absolute
      color:#fff
      bottom:-1rem
</style>
