<template>
    <div class="content">
        <Banner></Banner>
        <DetailHeader></DetailHeader>
    </div>
</template>
<script>
import Banner from './components/Banner'
import DetailHeader from './components/Header'
export default {
  name: 'Detail',
  components: {
    Banner,
    DetailHeader
  }

}
</script>
<style lang="stylus" scoped>
    .content
        height 50rem
</style>
