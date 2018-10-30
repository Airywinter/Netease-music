<template>
<div>
  <HomeHeader></HomeHeader>
  <HomeSwiper></HomeSwiper>
  <HomeIcons></HomeIcons>
  <HomeRecommand :recommandList="recommandList"></HomeRecommand>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommand from './components/Recommand'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommand
  },
  data () {
    return {
      recommandList: ''
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('http://localhost:3000/personalized')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      this.recommandList = res.result
      console.log(this.recommandList)
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style>

</style>
