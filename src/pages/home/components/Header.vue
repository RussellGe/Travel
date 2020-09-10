<template>
    <div class="header">
        <div class="header-left">
          <div class="iconfont back-icon">&#xe629;</div>
        </div>
        <div class="header-input">
          <span class="iconfont">&#xe610;</span>
          输入城市/景点/游玩主题
        </div>
        <div class="header-right">
          城市
          <span class="iconfont icon-arrow">&#xe6aa;</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        font-size: .4rem
        text-align: center
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      background: #fff
      padding-left: .2rem
      margin-left: .2rem
      border-radius: .1rem
      color: #cccccc
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .icon-arrow
        font-size: .24rem
        margin-left: -.04rem
</style>
