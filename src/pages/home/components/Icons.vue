<template>
<div class="icon-wrapper">
  <swiper :options="swiperOption" ref="mySwiper" v-show="list.length">
    <swiper-slide v-for="(page, index) in pages" :key="index">
      <div class="icons">
          <div class="icon" v-for="item in page" :key="item.id">
            <img class="icon-img" :src="item.imgUrl" alt="">
              <p class="icon-des">{{ item.desc }}</p>
          </div>

      </div>
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>

</div>

</template>
<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data () {
    return {
      // iconList: [1, 4, 5, 6, 2, 3, 4, 56, 77, 7]
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: false
      }
    }
  },
  computed: {
    pages () {
      const arr = []
      this.list.forEach((item, index) => {
        let page = Math.floor(index / 8)
        if (!arr[page]) {
          arr[page] = []
        }
        arr[page].push(item)
      })
      return arr
    }
  }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/variable.styl'

    .icons

        // background green
        overflow hidden
        .icon
            width 25%
            // padding-bottom 25%
            float left
            // background red
            display flex
            justify-content center
            align-items center
            flex-direction column
            padding-bottom 0.24rem
            .icon-img
                display block
                width 60%
                height auto
                padding-top .12rem
            .icon-des
                width 100%
                text-align center
                padding-top .12rem
                color $textColor
                font-size 0.26rem
                overflow hidden
                white-space nowrap
                text-overflow ellipsis
</style>
