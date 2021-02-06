<template>
  <div class="wrapper">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hot-recommend></home-hot-recommend>
    <home-raiders></home-raiders>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icon'
import HomeHotRecommend from './components/hotRecommend'
import HomeRaiders from './components/Raiders'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotRecommend,
    HomeRaiders
  }
}
</script>

<style>
</style>
