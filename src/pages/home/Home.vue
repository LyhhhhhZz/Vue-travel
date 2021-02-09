<template>
  <div class="home-wrapper">
    <home-header></home-header>
    <!-- <home-header :city="city"></home-header> -->
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-hot-recommend :list="recommendList"></home-hot-recommend>
    <home-raiders :list="radiersList"></home-raiders>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icon'
import HomeHotRecommend from './components/hotRecommend'
import HomeRaiders from './components/Raiders'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotRecommend,
    HomeRaiders
  },
  data () {
    return {
      // city: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      radiersList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.radiersList = data.radiersList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style>
</style>
