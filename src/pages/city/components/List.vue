<template>
    <div class="list" ref="wrapper">
       <div class="area">
           <div class="title border">当前城市</div>
           <div class="button-list">
               <div class="button-wrapper">
                   <div class="button">北京</div>
               </div>
           </div>
       </div>
       <div class="area">
           <div class="title border">热门城市</div>
           <div class="button-list">
               <div class="button-wrapper">
                   <div class="button">北京</div>
               </div>
               <div class="button-wrapper">
                   <div class="button">北京</div>
               </div>
               <div class="button-wrapper">
                   <div class="button">北京</div>
               </div>
               <div class="button-wrapper">
                   <div class="button">北京</div>
               </div>
               <div class="button-wrapper">
                   <div class="button">北京</div>
               </div>
           </div>
           
       </div>
       <div class="area">
           <div class="title border">A城市</div>
           <ul class="item-list">
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
           </ul>
       </div>
       <div class="area">
           <div class="title border">B</div>
           <ul class="item-list">
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
           </ul>
       </div>
       <div class="area">
           <div class="title border">C</div>
           <ul class="item-list">
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
                <li class="item">阿拉尔</li>
           </ul>
       </div>
    </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    console.log(this.$refs.wrapper)
    this.scroll = new Bscroll(this.$refs.wrapper,{
        pullUpLoad: true
    })  
  }
}
</script>
<style lang="stylus" scoped>
    @import "~styles/variable.styl"
    .list
        position absolute
        overflow hidden
        top 1.6rem
        left 0
        right 0
        bottom 0
        .border
            &:before 
                border-color #ccc
            &:after
                border-color #ccc
        .title
            line-height .54rem
            background #eee
            padding 0 0.3rem
            font-size 0.32rem
        .button-list
            padding .1rem
            padding-right .6rem
            display flex
            flex-wrap wrap
            .button-wrapper
                flex-basis 33.3%
                .button
                    margin .1rem
                    padding .1rem 0
                    text-align center
                    border 0.02rem solid #ccc
        .item
            padding 0.24rem 0
            padding-left 0.2rem
            border-bottom 0.02rem solid #eee
            font-size 0.28rem
            font-weight 600 
</style>
