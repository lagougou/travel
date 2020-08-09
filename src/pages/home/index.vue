<template>
    <div>
        <HomeHeader></HomeHeader>
        <HomeSwiper></HomeSwiper>
        <HomeIcons></HomeIcons>
        <HomeRecommend></HomeRecommend>
        <Weekend></Weekend>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import Weekend from './components/Weekend'
// import axios from 'axios'
export default {
  data () {
    return {}
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

  }
}
</script>

<style>

</style>
