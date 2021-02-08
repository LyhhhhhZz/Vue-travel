<template>
  <div class="radiers">
    <div class="title">旅游攻略</div>
    <div class="radiers-title">趣味亲子游</div>
    <div class="radiersItem" v-for="item of list" :key="item.id">
      <div class="radiersItem-img">
        <img :src="item.imgUrl" class="radiersItem-img-content">
      </div>
      <div class="radiersItem-content">
        <p class="radiersItem-desc">{{item.desc}}</p>
      </div>
    </div>
    <button class="radiers-btn">更多精彩攻略 ></button>
  </div>
</template>

<script>
export default {
  name: 'HomeRaiders',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
@import '~@/assets/styles/mixins.styl'
  .radiers
    position: relative
    height: 9.5rem
    .title
      margin-left: .3rem
      margin-top: .6rem
      color: #26282a
      font-weight: 700
      font-size: .36rem
    .radiers-title
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
    .radiers-btn
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
    .radiersItem
      position: relative
      overflow: hidden
      float: left
      width: 50%
      height: 0
      padding-bottom: 43%
      .radiersItem-img
        position: absolute
        top: 0
        left: 0
        right: 0
        box-sizing: border-box
        padding: 0 .1rem
        .radiersItem-img-content
          display: block
          border-radius: .2rem
          width: 100%
          margin: 0 auto
      .radiersItem-content
        position: absolute
        height: .8rem
        bottom: 0
        left: 0
        right: 0
        padding: 0 .3rem
        .recomendItem-desc
          display: block
          font-size: .14rem
          color: #000
          font-weight: 450
          ellipsis()

</style>
