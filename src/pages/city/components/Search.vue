<template>
  <div class="search">
     <input  class='search-input' type='text' placeholder='输入城市或者拼音'>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' scoped>
@import '~@/styles/varibles.styl'
.search
  height:.72rem
  background:$bgColor
  padding:0 .1rem
  .search-input
    width:100%
    line-height:.62rem
    box-sizing:border-box
    padding:0 .06rem
    color:#666
    text-align:center
    border-radius:.06rem
</style>
