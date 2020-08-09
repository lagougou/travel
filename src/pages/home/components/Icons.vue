<template>
    <div class="icons">
        <div class="icon">
            <img class="icon-img" src="http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png" alt="">
            <p class="icon-des">上海野生动物园啊啊啊</p>
        </div>
        <div class="icon">
            <img class="icon-img" src="https://img1.qunarzz.com/piao/fusion/1810/50/26ffa31b56646402.png" alt="">
            <p class="icon-des">上海海昌</p>
        </div>
        <div class="icon">
            <img class="icon-img" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" alt="">
            <p class="icon-des">景点门票</p>
        </div>
        <div class="icon">
            <img class="icon-img" src="http://img1.qunarzz.com/piao/fusion/1803/de/f26be47a6bf02a02.png" alt="">
            <p class="icon-des">上海迪士尼</p>
        </div>
        <div class="icon">
            <img class="icon-img" src="http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png" alt="">
            <p class="icon-des">东方明珠</p>
        </div>
        <div class="icon">
            <img class="icon-img" src="http://img1.qunarzz.com/piao/fusion/1803/8c/47630407f70e8302.png" alt="">
            <p class="icon-des">上海乐园</p>
        </div>
        <div class="icon">
            <img class="icon-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9480e99a101564a22dfff0c4b9d0861c.png" alt="">
            <p class="icon-des">上影乐园</p>
        </div>
        <div class="icon">
            <img class="icon-img" src="http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png" alt="">
            <p class="icon-des">酒店</p>
        </div>
    </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [1, 4, 5, 6, 2, 3, 4, 56, 77, 7]
    }
  },
  computed: {
    pages () {
      const arr = []
      this.iconList.forEach((item, index) => {
        let page = Math.floor(index / 8)
        if (!arr[page]) {
          arr[page] = []
        }
        arr[page].push(item)
      })
      return arr
    }
  }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/variable.styl'
    .icons

        // background green
        overflow hidden
        .icon
            width 25%
            // padding-bottom 25%
            float left
            // background red
            display flex
            justify-content center
            align-items center
            flex-direction column
            .icon-img
                display block
                width 60%
                height auto
                padding-top .12rem
            .icon-des
                width 100%
                text-align center
                padding-top .12rem
                color $textColor
                font-size 0.26rem
                overflow hidden
                white-space nowrap
                text-overflow ellipsis
</style>
