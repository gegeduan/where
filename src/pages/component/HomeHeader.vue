<template>
  <div class="header">
     <div class='header-left'>
       <span class='iconfont'>&#xe624;</span>
     </div>
     <div class='header-input'>
        <span class='iconfont'>&#xe632;</span>
       输入城市/景点/游玩主题
     </div>
     <router-link to='/city'>
        <div class='header-right'>
          {{this.city}}
          <span class='iconfont down-icon'>&#xe600;</span>
          </div>
     </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  // 把state的数据映射到computed属性里的city属性里
  computed: {
    ...mapState(['city'])
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
.header
  display:flex
  height:$HeaderHeight
  width:100%
  line-height:$HeaderHeight
  background:$bgColor
  color:#fff
  .header-left
    width:.68rem
    padding-left:.1rem
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
    min-width:1rem
    padding:0 .1rem
    text-align:center
    color:#fff
    .down-icon
      margin-left:-.15rem
      font-size:.34rem
</style>
