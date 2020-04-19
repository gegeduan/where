<template>
  <div class="header">
    城市选择
    <router-link to='/'>
      <div class='iconfont header-back'>&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' scoped>
@import '~@/styles/varibles.styl'
.header
  position:relative
  height:$HeaderHeight
  line-height:$HeaderHeight
  color:#fff
  font-size:.32rem
  background:$bgColor
  text-align:center
  .header-back
    position:absolute
    width:.64rem
    text-align:center
    top:0
    left:0
    font-size:.4rem
    color:#fff
</style>
