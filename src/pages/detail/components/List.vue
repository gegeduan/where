<template>
    <div class='list-wrapper'>
        <div class='list' v-for='(item, index) of list' :key='index'>
            <div class='item'>
                <span class='iconfont number-icont'>&#xe729;</span>
                {{item.title}}
                </div>
                <div class='children' v-if='item.children'>
                    <detail-list
                    :list='item.children'
                    v-for='(item, index) of list'
                    :key='index'>
                    {{item.title}}
                    </detail-list>
                </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  },
  data () {
    return {
    }
  },
  methods: {
  }
}
</script>

<style  lang='stylus' scoped>
.item
  height:.64rem
  line-height:.64rem
  padding:0 .1rem
  font-size:.32rem
.children
  padding:0 .2rem
</style>
