<template>
  <div class="list">
    <div class='item'>A</div>
    <div class='item'>A</div>
    <div class='item'>A</div>
    <div class='item'>A</div>
    <div class='item'>A</div>
    <div class='item'>A</div>
    <div class='item'>A</div>
    <div class='item'>A</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet',
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
