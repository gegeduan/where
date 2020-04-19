<template>
  <div class="list">
    <div class='item'
     v-for='item of letters'
     :key='item'
     @click='handleLetterClick'
     @touchstart.prevent='handleTouchStart'
     @touchmove='handleTouchMove'
     @touchend='handleTouchEnd'
     :ref='item'
     >{{item}}</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    listCities: Object
  },
  data () {
    return {
      touchStatus: false,
      startY: 0,
      timer: null
    }
  },
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.listCities) {
        letters.push(i)
      }
      return letters
    }
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        if (this.timer) {
          clearTimeout(this.timer)
        }
        this.timer = setTimeout(() => {
          const touchY = e.touches[0].clientY - 79
          const index = Math.floor((touchY - this.startY) / 20)
          if (index >= 0 && index < this.letters.length) {
            this.$emit('change', this.letters[index])
          }
        }, 16)
      }
    },
    handleTouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' scoped>
@import '~@/styles/varibles.styl'
.list
  position:absolute
  top:1.58rem
  right:0
  bottom:0
  display:flex
  flex-direction:column
  justify-content:center
  width:.44rem
  .item
    text-align:center
    line-height:.4rem
    color:$bgColor
</style>
