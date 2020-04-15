<template>
  <div class="detail">
   <detail-banner></detail-banner>
   <detail-header></detail-header>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  lang='stylus' scoped>
.detail
 height:50rem
</style>
