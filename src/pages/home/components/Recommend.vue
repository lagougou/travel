<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul>
            <router-link to="/detail">
            <li class="item" v-for="item in list" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" alt="" >
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
            </router-link>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
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
        overflow hidden
        display flex
        height 1.9rem
        // background red
        border-bottom 0.02rem solid #ccc
        .item-img
            width 1.7rem
            height 1.7rem
            padding 0.1rem
            // outline 1px solid blue
        .item-info
            flex 1
            padding .1rem
            box-sizing content-box
            // padding-top .5rem
            .item-title
                margin-top .2rem
                font-size .32rem
                font-weight 600
                color #333
            .item-desc
                margin-top .2rem
                font-size .26rem
                overflow hidden
                text-overflow ellipsis
                white-space nowrap
                width 70%
            .item-button
                background #ff9300
                padding 0 .1rem
                border-radius .1rem
                color #fff
                font-size .24rem
                margin-top .16rem
</style>
