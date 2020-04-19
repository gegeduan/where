<template>
  <div class="detail">
   <detail-banner
    :sightName='sightName'
    :bannerImg='bannerImg'
    :galleryImgs='galleryImgs'
     ></detail-banner>
   <detail-header></detail-header>
   <detail-list :list='list'></detail-list>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import axios from 'axios'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      sightName: '',
      bannerImg: '',
      galleryImgs: [],
      list: []
    }
  },
  methods: {
    getDetailInfo () {
      axios.get('/static/mock/detail.json', {
        params: {
          id: this.$route.id
        }
      }).then(this.handleGetDetailInfoSucc)
    },
    handleGetDetailInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.sightName = data.sightName
        this.bannerImg = data.bannerImg
        this.galleryImgs = data.gallaryImgs
        this.list = data.categoryList
        console.log(data)
      }
    }
  },

  mounted () {
    this.getDetailInfo()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  lang='stylus' scoped>
.detail
 height:50rem
</style>
