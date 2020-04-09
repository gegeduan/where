<template>
  <div class="weekend">
  <p class='title'>周末去哪</p>
  <ul>
      <li class='item border-bottom' v-for='(item, index) of list' :key='index'>
           <div class='img-wrapper'>
              <img class='item-img' :src='item.imgUrl'>
           </div>
          <div class='info'>
              <p class='info-title'>{{item.title}}</p>
              <p class='info-desc'>{{item.desc}}</p>
          </div>
      </li>
  </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' scoped>
@import '~@/styles/mixins.styl'
.title
  line-height:.8rem
  text-indent:.2rem
  font-size:.32rem
  background:#ccc
.item
  width:100%
  .img-wrapper
    overflow:hidden
    height:0
    padding-bottom:37.9%
    .item-img
      width:100%
  .info
    min-width:0
    margin-left:.2rem
    .info-title
        line-height:.54rem
        font-size:.32rem
        ellipsis()
    .info-desc
        line-height:.4rem
        color:#ccc
        padding-bottom:.1rem
        ellipsis()
</style>
