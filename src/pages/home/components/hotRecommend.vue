<template>
  <div class="recommend">
    <div class="title">特惠门票</div>
    <div class="recommend-title">当季热门度假</div>
    <div class="recommendItem" v-for="item of recommendList" :key="item.id">
      <div class="recommendItem-img">
        <img :src="item.imgUrl" class="recommendItem-img-content">
        <div class="recommendItem-img-desc">
          <div class="recommendItem-img-desc-wrapper">
            <div class="recommendItem-img-desc-addition">{{item.descAddition}}</div>
            <div class="recommendItem-img-desc-day">{{item.descDay}}</div>
          </div>
        </div>
      </div>
      <div class="recommendItem-content">
        <span class="recomendItem-desc">{{item.desc}}</span>
        <p class="recommendItem-price">{{item.price}}</p>
      </div>
    </div>
    <button class="recommend-btn">更多当季热门度假 ></button>
  </div>
</template>

<script>
export default {
  name: 'HomeHotRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: '//imgs.qunarzz.com/p/p67/1512/a2/0ebfcd965b9391f7.jpg_256x160_04d5813d.jpg',
        descAddition: '盐城 - 三亚',
        descDay: '5天跟团游',
        desc: '含往返飞机票+4晚住宿',
        price: '￥ 2950'
      },
      {
        id: '0002',
        imgUrl: '//imgs.qunarzz.com/p/p4/1809/50/c387c050d5188702.jpg_256x160_0d611436.jpg',
        descAddition: '盐城 - 苏州',
        descDay: '3天跟团游',
        desc: '含2晚住宿',
        price: '￥ 588'
      },
      {
        id: '0003',
        imgUrl: '//imgs.qunarzz.com/p/p70/1809/e7/4941057a6aae702.jpg_256x160_9fee6ccb.jpg',
        descAddition: '盐城 - 丽江',
        descDay: '5天跟团游',
        desc: '含往返飞机票+4晚住宿',
        price: '￥ 4960'
      },
      {
        id: '0004',
        imgUrl: '//imgs.qunarzz.com/p/p27/201302/28/d14185ac8a47f6f993835fbb.jpg_256x160_c2ab9336.jpg',
        descAddition: '盐城 - 张家界',
        descDay: '4天自由行',
        desc: '含往返飞机票+3晚住宿',
        price: '￥ 2290'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
@import '~@/assets/styles/mixins.styl'
  .recommend
    position: relative
    height: 9.5rem
    // background: red
    .title
      margin-left: .3rem
      margin-top: .6rem
      color: #26282a
      font-weight: 700
      font-size: .36rem
    .recommend-title
      width: 25%
      line-height: .6rem
      border-radius: .3rem
      background: $bgColor
      color: white
      padding: 0 .1rem
      margin-left: .2rem
      margin-top: .2rem
      margin-bottom: .2rem
      text-align: center
    .recommend-btn
      position: absolute
      bottom: 0
      left: 50%
      transform: translateX(-50%)
      width: 5rem
      height: 1rem
      margin-bottom: .2rem
      color: $bgColor
      font-weight: 400
      font-size: .32rem
      background: #fff
      border: .02rem solid $bgColor
    .recommendItem
      position: relative
      overflow: hidden
      float: left
      width: 50%
      height: 0
      padding-bottom: 43%
      // background: red
      .recommendItem-img
        position: absolute
        // overflow: hidden
        // border-radius: .1rem
        top: 0
        left: 0
        right: 0
        // bottom: .100rem
        box-sizing: border-box
        padding: 0 .1rem
        .recommendItem-img-content
          display: block
          border-radius: .2rem
          width: 100%
          margin: 0 auto
        .recommendItem-img-desc
          position: absolute
          bottom: 0
          left: 50%
          transform: translateX(-50%)
          background: black
          opacity: .7
          .recommendItem-img-desc-wrapper
            width: 2rem
            height: 1rem
            .recommendItem-img-desc-addition
              text-align: center
              padding-top: .2rem
              font-size: .14rem
              font-weight: 400
              font-family: Microsoft YaHei
              color: #fff
            .recommendItem-img-desc-day
              text-align: center
              padding-top: .1rem
              font-size: .1rem;
              font-weight: 400;
              font-family: Microsoft YaHei
              color: #ffde00;
      .recommendItem-content
        position: absolute
        height: .8rem
        bottom: 0
        left: 0
        right: 0
        padding: 0 .3rem
        // background-color: blue
        .recomendItem-desc
          display: block
          font-size: .14rem
          color: #000
          font-weight: 450
          ellipsis()
        .recommendItem-price
          margin-top: .1rem
          font-size: .30rem
          font-weight: 550
          color: #ff7400

</style>
