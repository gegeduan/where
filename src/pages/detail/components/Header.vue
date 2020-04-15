<template>
    <div class='header-wrapper'>
       <div class="header" v-show="!showAbs" :style="opacityStyle">
           详情查询
        <router-link to='/'>
          <div class='iconfont header-back'>&#xe624;</div>
        </router-link>
       </div>
        <router-link to='/'>
        <div class='iconfont icon-back' v-show='showAbs'>&#xe624;</div>
        </router-link>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = {
          opacity: opacity
        }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  }
}
</script>

<style  lang='stylus' scoped>
@import '~@/styles/varibles.styl'
.header
  position:fixed
  top:0
  left:0
  right:0
  height:$HeaderHeight
  line-height:$HeaderHeight
  color:#fff
  font-size:.32rem
  background:$bgColor
  text-align:center
  .header-back
    position:absolute
    width:.64
    line-height:.8rem
    text-align:center
    top:0
    left:.2rem
    font-size:.4rem
    color:#fff
.icon-back
  position:absolute
  width:.8rem
  height:.8rem
  line-height:.8rem
  border-radius:.4rem
  text-align:center
  top:0
  left:0
  font-size:.4rem
  color:#fff
  background:rgba(0, 0, 0, 0.8)
</style>
