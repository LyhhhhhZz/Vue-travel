<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont search-icon">&#xe632;</span>
      输入城市/景点/游玩主题</div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe600;</span></div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  .header
    display: flex
    height: .86rem
    line-height: .86rem
    background-color: $bgColor
    color: #fff
    .header-left
      position: relative
      width: .64rem
      float: left
      .back-icon
        position: absolute
        left: .12rem
        font-size: .4rem
    .header-input
      flex:  1
      line-height: .64rem
      border-radius: .1rem
      margin: .12rem .2rem
      background: #fff
      color: #ccc
      .search-icon
        margin-left: 0.2rem
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .arrow-icon
        margin-left: -.08rem
</style>
