<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont search-icon">&#xe632;</span>
      输入城市/景点/游玩主题</div>
    <router-link to='/city'>
      <div class="header-right">
        {{this.currentCity}}
        <span class="iconfont arrow-icon">&#xe600;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState({
      currentCity: 'city'
    })
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  .header
    display: flex
    height: $headerHeight
    line-height: $headerHeight
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
      min-width: 1.24rem
      padding: 0 .1rem
      float: right
      text-align: center
      color: white
      .arrow-icon
        margin-left: -.08rem
</style>
