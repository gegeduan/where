<template>
    <div class='icons'>
       <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
       <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
        <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
       <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
       <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
       <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
        <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
       <div class='icon'>
           <div class='icon-img'>
               <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'>
           </div>
           <p class='icon-desc'>热门景点</p>
       </div>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
    }
  }
}
</script>
<style lang='stylus' scoped>
@import '~@/styles/varibles.styl'
.icons
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
            color:$fontTextColor

</style>
