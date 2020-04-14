<template>
  <div class="list" ref='wrapper'>
      <div>
            <div class='area border-topbottom'>
                <div class='title'>当前城市</div>
                <div class='btn-list'>
                <div class='btn'>{{this.city}}</div>
                </div>
            </div>
            <div class='area border-topbottom'>
                <div class='title'>热门城市</div>
                <div class='btn-list'>
                <div class='btn'
                 v-for='item of listHotCities'
                 :key='item.id'
                 @click='handleClick(item.name)'
                  >{{item.name}}</div>
                </div>
            </div>
            <div class='area border-topbottom'
            v-for='(item, key) of listCities'
            :key='key'
            :ref='key'
            >
                <div class='title'>{{key}}</div>
                <div class='item-list'>
                <div class='item border-bottom'
                 v-for='ite of item'
                  :key='ite.id'
                  @click='handleClick(ite.name)'
                  >{{ite.name}}</div>
                </div>
            </div>
     </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
import { mapState } from 'vuex'
export default {
  name: 'CityList',
  props: {
    listCities: Object,
    listHotCities: Array,
    ListLetter: String
  },
  data () {
    return {
    }
  },
  // 把state的数据映射到computed属性里的city属性里
  computed: {
    ...mapState(['city'])
  },
  methods: {
    handleClick (city) {
      this.$store.dispatch('changeCity', city)
      this.$router.push('/')
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  },
  watch: {
    ListLetter () {
      if (this.ListLetter) {
        const element = this.$refs[this.ListLetter][0]
        this.scroll.scrollToElement(element)
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
.list
  position:absolute
  overflow:hidden
  top:1.58rem
  left:0
  right:0
  bottom:0
  .area
    .title
      padding-left:.2rem
      height:.54rem
      line-height:.54rem
      color:#666
      font-size:.26rem
      background:#eee
    .btn-list
      overflow:hidden
      padding:.1rem .6rem .1rem .1rem
      .btn
        float:left
        box-sizing:border-box
        padding:.1rem
        border-radius:.06rem
        width:30%
        margin:.05rem
        text-align:center
        border:.02rem solid #ccc
    .item-list
      .item
        padding-left:.2rem
        line-height:.54rem
        color:#666
</style>
