<template>
    <div>
        <router-link to="/" v-show="showHeader">
            <div class="header-abs"><span class="iconfont back-icon">&#xe624;</span></div>
        </router-link>
            <div class="header-fixed" v-show="!showHeader" :style="opacityStyle">
                <router-link to="/">
            <div class="iconfont header-fixed-back">&#xe624;</div>
        </router-link>
        景点详情
        </div>
    </div>
</template>
<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showHeader: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      console.log(top)
      if (top > 60) {
        this.showHeader = false
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = {opacity}
      } else {
        this.showHeader = true
      }
    }

  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/variable.styl'
    .header-abs
        position absolute
        left .2rem
        top .2rem
        width .8rem
        height .8rem
        border-radius .4rem
        background-color rgba(0,0,0, .8)
        text-align center
        line-height .8rem
        .back-icon
            color #fff
    .header-fixed
        position fixed
        top 0
        left 0
        right 0
        height 0.86rem
        line-height 0.86rem
        text-align center
        color #fff
        font-size .32rem
        background-color $bgColor
        .header-fixed-back
            position: absolute
            top: 0
            left: 0
            width: .64rem
            text-align: center
            font-size: .4rem
            color: #fff
</style>
