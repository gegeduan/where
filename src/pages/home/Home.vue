<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
  </div>
</template>

<script>
import HomeHeader from '@/pages/component/HomeHeader'
import HomeSwiper from '@/pages/component/Swiper'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  scoped>
</style>
