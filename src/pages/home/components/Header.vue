<template>
    <div class="header">
        <div class="header-left"><span class="iconfont back-icon">&#xe624;</span></div>
        <div class="header-input"><span class="iconfont search-icon">&#xe632;</span>输入/城市/景点</div>
        <router-link to="/city">
            <div class="header-right">城市<span class="iconfont arrow-down">&#xe64a;</span></div>
        </router-link>
    </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
    @import '~styles/variable.styl'
    .header
        display: flex
        background-color: $bgColor
        color: #fff
        height: 0.86rem
        line-height .86rem
        .header-left
            width: .64rem
            float: left
            .back-icon
                display block
                font-size .4rem
        .header-input
            flex: 1
            background-color #fff
            border-radius 0.1rem
            margin-left .2rem
            margin-top 0.12rem
            margin-bottom  0.12rem
            color #ccc
            line-height .64rem
            text-align left
            padding-left .1rem
            .search-icon
                margin-right .1rem
        .header-right
            width 1.24rem
            float right
            text-align center
            color #fff
            .arrow-down
                margin-left .05rem
                font-size .24rem

</style>
