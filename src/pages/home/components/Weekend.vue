<template>
    <div>
        <div class="recommend-title">
            周末去哪儿
        </div>
        <ul>
            <li class="item">
                <div class="item-img-wrapper">
                    <img src="http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg" alt="" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">上海必打卡</p>
                    <p class="item-desc">中西合璧，现代和传统各有各的精彩</p>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img src="http://img1.qunarzz.com/sight/source/1603/ad/69b0fc5f48ad5f.jpg_r_640x214_b0fd5c7b.jpg" alt="" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">周末亲子爱玩</p>
                    <p class="item-desc">走进自然或玩转乐园，感知大千世界，游乐项目惊险刺激，特色表演异彩纷呈，等你们~</p>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img src="http://img1.qunarzz.com/sight/source/1505/7b/2a6b0ce087f0e5.jpg_r_640x214_5c76b115.jpg" alt="" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">情迷博物馆</p>
                    <p class="item-desc">走进艺术殿堂，电影博物馆生动演绎着电影人和电影背后的故事，你不想知道吗~</p>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img src="http://img1.qunarzz.com/sight/source/1511/1d/fe098e8cfec117.jpg_r_640x214_a9be292a.jpg" alt="" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">上海城市观光</p>
                    <p class="item-desc">来这里寻找你所不认识的魔都 ，感受云端漫步，品味老上海风情，享受休闲时光~</p>
                </div>
            </li>
            <li class="item">
                <div class="item-img-wrapper">
                    <img src="http://img1.qunarzz.com/sight/source/1505/6f/2711e071838590.jpg_r_640x214_8f1ad9a1.jpg" alt="" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">戏水清凉一夏</p>
                    <p class="item-desc">夏日戏水，玩“乐”无穷</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'Weekend'
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
