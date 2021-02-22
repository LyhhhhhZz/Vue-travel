<template>
  <div>
    <div class="banner">
      <img class="banner-img" src="https://imgs.qunarzz.com/vs_ceph_b2c_001/bc076dde-ed2d-47ef-97b7-97d39d13f3a5.jpg_r_390x260x95_9b189a2a.jpg">
      <div class="banner-info">
        <div class="banner-tittle">上天入海嗨翻三亚</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe632;</span>
          10
        </div>
      </div>
    </div>
    <common-gallary></common-gallary>
  </div>
</template>

<script>
import CommonGallary from '../../../common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top,
      rgba(0, 0, 0, 0) , rgba(0, 0, 0, 0.8))
      .banner-tittle
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        margin-top: .14rem
        margin-right: .3rem
        padding: 0 .4rem
        line-height: .32rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
