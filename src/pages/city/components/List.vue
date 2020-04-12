<template>
  <div class="list">
    <div class='area border-topbottom'>
        <div class='title'>当前城市</div>
        <div class='btn-list'>
          <div class='btn'>北京</div>
           <div class='btn'>北京</div>
           <div class='btn'>北京</div>
           <div class='btn'>北京</div>
        </div>
    </div>
     <div class='area border-topbottom'>
        <div class='title'>当前城市</div>
        <div class='btn-list'>
          <div class='btn'>北京</div>
           <div class='btn'>北京</div>
           <div class='btn'>北京</div>
           <div class='btn'>北京</div>
        </div>
    </div>
    <div class='area border-topbottom'>
        <div class='title'>A</div>
        <div class='item-list'>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
        </div>
        <div class='title'>A</div>
        <div class='item-list'>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
        </div>
        <div class='title'>A</div>
        <div class='item-list'>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
        </div>
        <div class='title'>A</div>
        <div class='item-list'>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
           <div class='item border-bottom'>阿拉尔</div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityList',
  data () {
    return {
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
      height:.44rem
      line-height:.44rem
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
