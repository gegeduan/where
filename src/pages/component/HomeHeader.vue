<template>
  <div class="header">
     <div class='header-left'>
       <span class='iconfont'>&#xe624;</span>
     </div>
     <div class='header-input'>
        <span class='iconfont'>&#xe632;</span>
       输入城市/景点/游玩主题
     </div>
      <div class='header-right'>
        城市
        <span class='iconfont down-icon'>&#xe600;</span>

        </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
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
  display:flex
  height:0.86rem
  width:100%
  line-height:.86rem
  background:$bgColor
  color:#fff
  .header-left
    width:.68rem
    .back-icon
      text-align:center
      font-size:.4rem
  .header-input
    margin-top:.12rem
    padding-left:.2rem
    flex:1
    height:.62rem
    line-height:.62rem
    background:#fff
    border-radius:.1rem
    color:#ccc
  .header-right
    width:1.2rem
    text-align:center
    .down-icon
      margin-left:-.15rem
      font-size:.34rem
</style>
