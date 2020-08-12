<template>
    <div class="header">
        <router-link to="/">
        <span class="iconfont back-icon">&#xe624;</span></router-link>城市选择
    </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
    @import "~styles/variable.styl"
    .header
        position relative
        overflow hidden
        height 0.86rem
        text-align center
        color #fff
        background $bgColor
        line-height 0.86rem
        font-size 0.32rem
        .back-icon
            width .64rem
            top 0
            left 0
            position absolute
            text-align center
            font-size .4rem
            color #fff
</style>
