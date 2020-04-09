<template>
  <div class="weekend">
  <p class='title'>周末去哪</p>
  <ul>
      <li class='item border-bottom' v-for='(item, index) of weekendList' :key='index'>
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
  data () {
    return {
      weekendList: [
        {
          id: '0003',
          title: '浦江郊野公园奇迹花园',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/cf/762cb38938a093.jpg_r_640x214_e02c18ef.jpg',
          desc: '这里现在很火很多人都在评论它,快来一起开心吧.这里现在很火很多人都在评论它,快来一起开心吧.'
        },
        {
          id: '0002',
          title: '浦江郊野公园奇迹花园',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/cf/762cb38938a093.jpg_r_640x214_e02c18ef.jpg',
          desc: '这里现在很火很多人都在评论它,快来一起开心吧.这里现在很火很多人都在评论它,快来一起开心吧.'
        },
        {
          id: '0003',
          title: '浦江郊野公园奇迹花园',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/cf/762cb38938a093.jpg_r_640x214_e02c18ef.jpg',
          desc: '这里现在很火很多人都在评论它,快来一起开心吧.这里现在很火很多人都在评论它,快来一起开心吧.'
        },
        {
          id: '0002',
          title: '浦江郊野公园奇迹花园',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/cf/762cb38938a093.jpg_r_640x214_e02c18ef.jpg',
          desc: '这里现在很火很多人都在评论它,快来一起开心吧.这里现在很火很多人都在评论它,快来一起开心吧.'
        },
        {
          id: '0003',
          title: '浦江郊野公园奇迹花园',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/cf/762cb38938a093.jpg_r_640x214_e02c18ef.jpg',
          desc: '这里现在很火很多人都在评论它,快来一起开心吧.这里现在很火很多人都在评论它,快来一起开心吧.'
        },
        {
          id: '0002',
          title: '浦江郊野公园奇迹花园',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/cf/762cb38938a093.jpg_r_640x214_e02c18ef.jpg',
          desc: '这里现在很火很多人都在评论它,快来一起开心吧.这里现在很火很多人都在评论它,快来一起开心吧.'
        }
      ]
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
    padding-bottom:33.9%
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
