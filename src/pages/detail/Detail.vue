<template>
  <div class="detail">
   <detail-banner></detail-banner>
   <detail-header></detail-header>
   <detail-list :list='list'></detail-list>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [
        {
          title: '成人票',
          children: [{
            title: '成人三馆联票',
            children: [
              {
                title: '成人三馆联票1'
              },
              {
                title: '成人三馆联票2'
              }
            ]
          },
          {
            title: '成人五馆联票'
          },
          {
            title: '成人七馆联票'
          }
          ]
        },
        {
          title: '儿童票'
        },
        {
          title: '特惠票'
        },
        {
          title: '老人票'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  lang='stylus' scoped>
.detail
 height:50rem
</style>
