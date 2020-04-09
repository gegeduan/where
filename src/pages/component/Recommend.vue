<template>
  <div class="recommend">
  <p class='title'>热门推荐</p>
  <ul>
      <li class='item border-bottom' v-for='(item, index) of list' :key='index'>
          <img class='item-img' :src='item.imgUrl'>
          <div class='info'>
              <p class='info-title'>{{item.title}}</p>
              <p class='info-desc'>{{item.desc}}</p>
              <button class='info-button'>查看详情</button>
          </div>
      </li>
  </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRcommend',
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
  display:flex
  padding:.2rem
  width:100%
.item-img
    width:1.7rem
    height 1.7rem
.info
    flex:1
    min-width:0
    margin-left:.2rem
    .info-title
      line-height:.54rem
      font-size:.32rem
      ellipsis()
    .info-desc
      line-height:.4rem
      color:#ccc
      ellipsis()
    .info-button
      padding:0 .2rem
      line-height:.44rem
      background:#ff9300
      border-radius:.06rem
      color:#fff
</style>
