<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe622;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe647;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市<span class="iconfont arrow-icon">&#xe6aa;</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .header
    background $bgColor
    color #fff
    line-height .88rem
    display flex
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      height .64rem
      line-height .64rem
      background #fff
      color #ccc
      border-radius .1rem
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
      flex 1
    .header-right
      min-width  1.04rem
      padding 0 .1rem
      float right
      text-align center
      color #fff
      .arrow-icon
        margin-left -.04rem
        font-size .24rem
</style>
