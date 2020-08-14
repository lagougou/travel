<template>
    <div>
        <HomeHeader></HomeHeader>
        <HomeSwiper :list="swiperList"></HomeSwiper>
        <HomeIcons :list="iconList"></HomeIcons>
        <HomeRecommend :list="recommendList"></HomeRecommend>
        <Weekend :list="weekendList"></Weekend>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import Weekend from './components/Weekend'
import axios from 'axios'
export default {
  data () {
    return {
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    Weekend
  },
  mounted () {
    this.getRecommend()
  },
  methods: {
    getRecommend () {
      axios.get('/api/index.json').then(this.getResult)
    },
    getResult (res) {
      let data = res.data
      if (data.ret && data.data) {
        console.log(data)
        this.swiperList = data.data.swiperList
        this.iconList = data.data.iconList
        this.recommendList = data.data.recommendList
        this.weekendList = data.data.weekendList
      }
    }
  }
}
</script>

<style>

</style>
