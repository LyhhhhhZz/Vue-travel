<template>
  <div>
    <div class="search">
      <input v-model="keyword" class="search-input" type="text" placeholder="输入城市名或拼音">
    </div>
    <div class="search-content">
      <ul>
        <li>{{this.keyword}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setTimeout(() => {

      }, 100)
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
  .search
    height: .72rem
    padding: 0 .2rem
    background: $bgColor
    .search-input
      box-sizing: border-box
      width: 100%
      padding: 0 .2rem
      height: .62rem
      line-height: .62rem
      text-align: center
      border-radius: .06rem
      color: #666
  .search-content
    overflow: hidden
    z-index: 1
    position: absolute
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    background: green
</style>
