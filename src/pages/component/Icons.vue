<template>
    <div class='icons'>
       <swiper>
           <swiper-slide v-for='(single,index) of pages ' :key='index'>
                <div class='icon' v-for='item of single' :key='item.id'>
                    <div class='icon-img'>
                        <img class='icon-img-content' :src='item.imgUrl'>
                    </div>
                    <p class='icon-desc'>{{item.desc}}</p>
                </div>
           </swiper-slide>
       </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [
        {
          id: '0001',
          desc: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: '0002',
          desc: '顾村赏樱',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/91a810441506568937171df66f754375.png'

        },
        {
          id: '0003',
          desc: '景点门票景点门票景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: '0004',
          desc: '顾村赏樱',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/91a810441506568937171df66f754375.png'

        },
        {
          id: '0005',
          desc: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: '0006',
          desc: '顾村赏樱',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/91a810441506568937171df66f754375.png'

        },
        {
          id: '0007',
          desc: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: '0008',
          desc: '顾村赏樱',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/91a810441506568937171df66f754375.png'

        },
        {
          id: '0005',
          desc: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: '0006',
          desc: '顾村赏樱',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/91a810441506568937171df66f754375.png'

        },
        {
          id: '0007',
          desc: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: '0008',
          desc: '顾村赏樱',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/91a810441506568937171df66f754375.png'

        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang='stylus' scoped>
@import '~@/styles/varibles.styl'
@import '~@/styles/mixins.styl'
.icons >>> .swiper-container
    overflow:hidden
    width:100%
    height:0
    padding-bottom:50%
    background:#eee
.icon
    overflow:hidden
    position:relative
    float:left
    width:25%
    height:0
    padding-bottom:25%
    .icon-img
        position:absolute
        top:0
        left:0
        right:0
        bottom 0.44rem
        padding:.1rem
        box-sizing:border-box
        padding:.1rem
        .icon-img-content
            display:block
            height:100%
            margin:0 auto
    .icon-desc
        position:absolute
        width:100%
        left:0
        right:0
        bottom:0
        height:.44rem
        line-height:.44rem
        text-align:center
        ellipsis()
        color:$fontTextColor

</style>
