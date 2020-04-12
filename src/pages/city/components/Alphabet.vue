<template>
  <div class="list">
    <div class='item' v-for='(item, key) of listCities' :key='key'>{{key}}</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    listCities: Object
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
.list
  position:absolute
  top:1.58rem
  right:0
  bottom:0
  display:flex
  flex-direction:column
  justify-content:center
  width:.44rem
  .item
    text-align:center
    line-height:.4rem
    color:$bgColor
</style>
