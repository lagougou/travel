<template>
    <div>
        <div class="recommend-title">
            周末去哪儿
        </div>
        <ul>
            <li class="item" v-for="item in list" :key="item.id">
                <div class="item-img-wrapper">
                    <img :src="item.imgUrl" alt="" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'Weekend',
  props: {
    list: Array
  }
}
</script>
<style lang="stylus" scoped>
    .recommend-title
        line-height 0.8rem
        background #eee
        text-indent .2rem
        margin-top .2rem
    .item
        border-bottom .08rem solid #eee
        .item-img
            height 2.4rem
        .item-info
            padding .32rem 0
            padding-left .24rem
            .item-title
                color #212121
                padding-top .1rem
                font-size .28rem
                overflow hidden
                text-overflow ellipsis
                white-space nowrap
            .item-desc
                padding-top .1rem
                margin-top .14rem
                color #616161
                font-size .24rem
                overflow hidden
                text-overflow ellipsis
                white-space nowrap
                padding-right  1.4rem
</style>
