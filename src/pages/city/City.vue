<template>
  <div class="city">
      <city-header></city-header>
      <city-search></city-search>
      <city-list></city-list>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' scoped>
</style>
