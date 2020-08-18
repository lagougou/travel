<template>
<div>
    <div class="banner" @click="handleClick">
        <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_600x330_bf9c4904.jpg" alt="">
        <div class="banner-info">
            <div class="info-title">大连圣亚海洋世界(AAAA景区)</div>
            <div class="info-number"><span class="iconfont banner-icon">&#xe61a;</span>39</div>
        </div>
    </div>
    <Fade>
        <Gallary :imgs="imgs" v-show="showGallary" @hide="hideGallary"></Gallary>
    </Fade>

</div>
</template>
<script>
import Gallary from '@/common/gallary/Gallary'
import Fade from '@/common/fade/Fade'
export default {
  name: 'DetailBanner',
  components: {
    Gallary,
    Fade
  },
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_600x330_bf9c4904.jpg', 'http://img1.qunarzz.com/sight/p0/1709/76/7691528bc7d7ad3ca3.img.png_800x800_9ef05ee7.png'],
      showGallary: false
    }
  },
  methods: {
    handleClick () {
      this.showGallary = true
    },
    hideGallary () {
      this.showGallary = false
    }
  }
}
</script>
<style lang="stylus" scoped>
    .banner
        position relative
        overflow hidden
        height 0
        padding-bottom 55%
        .banner-img
            width 100%
        .banner-info
            display flex
            position absolute
            left 0
            right 0
            bottom 0
            line-height .6rem
            color #fff
            padding-right .2rem
            .info-title
                padding-left .4rem
                flex 1
            .info-number
                // padding 0.4rem
                padding 0 .4rem
                height .4rem
                line-height .4rem
                border-radius .2rem
                background rgba(0,0,0, 0.8)
                font-size .24rem
                margin-top .08rem
                .iconfont
                    font-size .24rem
                    margin-right .14rem
</style>
