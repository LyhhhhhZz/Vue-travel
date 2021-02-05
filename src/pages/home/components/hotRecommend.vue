<template>
  <div class="recommend">
    <div class="recommend-title">当季热门度假</div>
    <div class="recommendItem">
      <div class="recommendItem-img">
        <img src="//imgs.qunarzz.com/p/p67/1512/a2/0ebfcd965b9391f7.jpg_256x160_04d5813d.jpg" class="recommendItem-img-content">
      </div>
      <div class="recommendItem-content">
        <span class="recomendItem-desc">222</span>
        <p>111</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHotRecommend'
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
  .recommend-title
    width: 25%
    line-height: .6rem
    border-radius: .3rem
    background: $bgColor
    color: white
    padding: .1rem
    margin-left: .2rem
    margin-top: .2rem
    margin-bottom: .2rem
    text-align: center
  .recommendItem
    position: relative
    overflow: hidden
    float: left
    width: 50%
    height: 0
    padding-bottom: 50%
    background: red
    .recommendItem-img
      position: absolute
      top: 0
      left: 0
      right: 0
      // bottom: .44rem
      box-sizing: border-box
      padding: 0 .1rem
      .recommendItem-img-content
        display: block
        width: 100%
        margin: 0 auto
    .recommendItem-content
      position: absolute
      bottom: 0
      left: 0
      right: 0
      padding: 0 .1rem
      background-color: blue;
</style>
