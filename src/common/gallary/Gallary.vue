<template>
  <div class="container">
    <div class="wrapper">
      <swiper ref="mySwiper" :options="swiperOptions">
        <swiper-slide
          v-for="(item, index) in imgs"
          :key="index">
          <img class="gallary-img" :src="item"/>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallary',
  props: {
    imgs: {
      type: Array,
      default () {
        return ['https://imgs.qunarzz.com/vs_ceph_b2c_001/bc076dde-ed2d-47ef-97b7-97d39d13f3a5.jpg_r_390x260x95_9b189a2a.jpg', 'https://imgs.qunarzz.com/vs_ceph_b2c_001/bc076dde-ed2d-47ef-97b7-97d39d13f3a5.jpg_r_390x260x95_9b189a2a.jpg']
      }
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow: inherit
  .container
    display: flex
    flex-direction: column
    justify-content: center
    z-index: 99
    position: fixed
    left: 0
    right: 0
    top: 0
    bottom: 0
    background: #000
    .wrapper
      height: 0
      width: 100%
      padding-bottom: 66%
      .gallary-img
        width: 100%
      .swiper-pagination
        bottom: -2rem
        color: #fff
</style>
