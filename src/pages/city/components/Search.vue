<template>
  <div class="search">
     <input class='search-input'
      type='text'
      v-model="keyword"
      placeholder='输入城市或者拼音'>
     <div class='search-content' ref='search' v-show='keyword'>
         <div>
            <div class='item-content border-bottom'
            v-for='item of list'
            :key='item.id'
            >{{item.name}}</div>
            <div class='item-content border-bottom' v-show='hasNoData '>没有找到匹配项</div>
         </div>
     </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  computed: {
    hasNoData () {
      return !this.list.length
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  }
}
</script>

<style lang='stylus' scoped>
@import '~@/styles/varibles.styl'
.border-topbottom
   &:before
     border-color:#777
   &:after
     border-color:#777
.border-bottom
   &:before
     border-color:#777
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
  .search-content
    z-index:100
    overflow:hidden
    position:absolute
    top:1.58rem
    left:0
    right:0
    bottom:0
    background:#eee
    .item-content
      color:#666
      padding-left:.2rem
      line-height:.62rem
      background:#fff
</style>
