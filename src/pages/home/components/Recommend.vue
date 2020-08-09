<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul>
            <li class="item">
                <div class="item-img-wrapper">
                    <img class="item-img" src="http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg" alt="" >
                </div>
                <div class="item-info">
                    <p class="item-title">上海迪士尼乐园</p>
                    <p class="item-desc">中西合璧，现代和传统各有各的精彩</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img class="item-img" src="http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg" alt="" >
                </div>
                <div class="item-info">
                    <p class="item-title">上海迪士尼乐园</p>
                    <p class="item-desc">中西合璧，现代和传统各有各的精彩</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img class="item-img" src="http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg" alt="" >
                </div>
                <div class="item-info">
                    <p class="item-title">上海迪士尼乐园</p>
                    <p class="item-desc">中西合璧，现代和传统各有各的精彩</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img class="item-img" src="http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg" alt="" >
                </div>
                <div class="item-info">
                    <p class="item-title">上海迪士尼乐园</p>
                    <p class="item-desc">中西合璧，现代和传统各有各的精彩</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img class="item-img" src="http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg" alt="" >
                </div>
                <div class="item-info">
                    <p class="item-title">上海迪士尼乐园</p>
                    <p class="item-desc">中西合璧，现代和传统各有各的精彩</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img class="item-img" src="http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg" alt="" >
                </div>
                <div class="item-info">
                    <p class="item-title">上海迪士尼乐园</p>
                    <p class="item-desc">中西合璧，现代和传统各有各的精彩</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'HomeRecommend'
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
            // box-sizing border-box
            // padding-top .5rem

            .item-title
                margin-top .2rem
                font-size .32rem
                font-weight 600
                color #333
            .item-desc
                margin-top .2rem
                font-size .26rem
            .item-button
                background #ff9300
                padding 0 .1rem
                border-radius .1rem
                color #fff
                font-size .24rem
                margin-top .16rem
</style>
