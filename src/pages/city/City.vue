<template>
  <div class="city-wrapper">
    <city-header></city-header>
    <city-search :cities='cities'></city-search>
    <city-list
    :cities='cities'
    :hotCities='hotCities'
    :letter='letter'></city-list>
    <city-alphabet
    :cities='cities'
    @change="handleLetterChange"></city-alphabet>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
import axios from 'axios'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data () {
    return {
      cities: {},
      hotCities: [],
      letter: ''
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    },
    handleLetterChange (letter) {
      this.letter = letter
    }
  },
  mounted () {
    this.getCityInfo()
    // document.addEventListener('touchstart', function (event) {
    //   if (event.cancelable) {
    //     // 判断默认行为是否已经被禁用
    //     if (!event.defaultPrevented) {
    //       event.preventDefault()
    //     }
    //   }
    // }, false)
  }
}
</script>

<style lang="stylus" scoped>

</style>
