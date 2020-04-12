<template>
  <div class="city">
      <city-header></city-header>
  </div>
</template>

<script>
import CityHeader from './components/Header'
export default {
  name: 'City',
  components: {
    CityHeader
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' scoped>
@import '~@/styles/varibles.styl'
</style>
