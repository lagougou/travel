<template>
    <div class="search">
        <input class="search-input" type="text" placeholder="输入城市名或拼音" />
    </div>
</template>
<script>
export default {
  name: 'CitySearch'
}
</script>
<style lang="stylus" scoped>
    @import "~styles/variable.styl"
    .search
        height 0.72rem
        background $bgColor
        padding 0 .1rem
        .search-input
            height .62rem
            line-height .62rem
            text-align center
            width 100%
            box-sizing border-box
            border-radius 0.06rem
            padding 0 0.1rem
</style>
