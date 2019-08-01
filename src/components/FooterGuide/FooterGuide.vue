<template>
  <div class="footer-guide">
    <a href="javascript:;" class="guide-item" :class="{on:'/home'===$route.path}" @click="goTo('/home')">
      <span class="item-icon">
        <i class="iconfont icon-waimai"></i>
      </span>
      <span>外卖</span>
    </a>
    <a href="javascript:;" class="guide-item" :class="{on:'/search'===$route.path}" @click="goTo('/search')">
      <span class="item-icon">
        <i class="iconfont icon-search"></i>
      </span>
      <span>搜索</span>
    </a>
    <a href="javascript:;" class="guide-item" :class="{on:'/order'===$route.path}" @click="goTo('/order')">
      <span class="item-icon">
        <i class="iconfont icon-dingdan"></i>
      </span>
      <span>订单</span>
    </a>
    <a href="javascript:;" class="guide-item" :class="{on:'/person'===$route.path}" @click="goTo('/person')">
      <span class="item-icon">
        <i class="iconfont icon-geren"></i>
      </span>
      <span>我的</span>
    </a>
  </div>
</template>

<script>
  export default {
    methods:{
      goTo(path){
        this.$router.replace(path)
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixins.styl"
  .footer-guide
    top-border-1px(#e4e4e4)
    position fixed
    left 0
    right 0
    bottom 0
    width 100%
    height 50px
    background-color #fff
    display flex
    .guide-item
      display flex
      flex 1
      text-align center
      flex-direction column
      align-items center
      margin 5px
      color #999999
      &.on
        color #02a774
      span
        font-size 12px
        margin 2px 0
        .iconfont
          font-size 22
</style>
