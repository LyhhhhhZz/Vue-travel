<template>
  <div class="wrapper">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hot-recommend></home-hot-recommend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icon'
import HomeHotRecommend from './components/hotRecommend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotRecommend
  }
}
</script>

<style>
</style>
