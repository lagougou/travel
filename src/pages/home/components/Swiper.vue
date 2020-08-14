<template>
<div class="wrapper">
    <swiper :options="swiperOption" :not-next-tick="notNextTick" ref="mySwiper" v-show="list.length">
    <!-- slides -->
    <swiper-slide v-for="item in list" :key="item.id">
      <img :src="item.imgUrl" alt="" class="swiper-img">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>

</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      // NotNextTick is a component's own property, and if notNextTick is set to true, the component will not instantiate the swiper through NextTick, which means you can get the swiper object the first time (if you need to use the get swiper object to do what Things, then this property must be true)
      // notNextTick是一个组件自有属性，如果notNextTick设置为true，组件则不会通过NextTick来实例化swiper，也就意味着你可以在第一时间获取到swiper对象，假如你需要刚加载遍使用获取swiper对象来做什么事，那么这个属性一定要是true
      notNextTick: false,
      swiperOption: {
        // swiper options 所有的配置同swiper官方api配置
        pagination: '.swiper-pagination',
        autoplay: 2500,
        loop: true
        // more Swiper configs and callbacks...
        // ...
      }
    }
  }
  // you can find current swiper instance object like this, while the notNextTick property value must be true
  // 如果你需要得到当前的swiper对象来做一些事情，你可以像下面这样定义一个方法属性来获取当前的swiper对象，同时notNextTick必须为true
}
</script>
<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet
        background-color white
    .wrapper >>> .swiper-container
        height 100%
    .wrapper
        width 100%
        height 2rem
        overflow hidden
        // padding-bottom 31.25%
        .swiper-img
            width 100%
            // height auto
</style>
