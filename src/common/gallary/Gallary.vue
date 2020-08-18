<template>
    <div class="container" @click="hideGallary">
        <div class="gallary">
             <swiper :options="swiperOption" ref="mySwiper">
    <!-- slides -->
                <swiper-slide v-for="(item,index) in imgs" :key="index">
                <img width="gallary-img" :src="item" alt="" class="swiper-img">

                </swiper-slide>
                <!-- Optional controls -->
                <div class="swiper-pagination"  slot="pagination"></div>

            </swiper>
        </div>
    </div>
</template>
<script>
export default {
  name: 'Gallary',
  props: {
    imgs: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observeParents: true,
        observer: true
      }
    }
  },
  methods: {
    hideGallary () {
      this.$emit('hide')
    }
  }
}
</script>
<style lang="stylus" scoped>
    .gallary >>> .swiper-pagination
        color #fff
    .gallary >>> .swiper-container
        height 100%
    .container
        display flex
        flex-direction column
        justify-content center
        position fixed
        z-index 99
        left 0
        right 0
        bottom 0
        top 0
        background-color #000
        .gallary
            // overflow hidden
            height 6rem
            .swiper-img
                height  100%
                width 100%
            .gallary-img
                width 100%
                height 100%
</style>
