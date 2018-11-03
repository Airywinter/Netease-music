<template>
<div>
  <Header></Header>
  <HomeSwiper :banner="banner"></HomeSwiper>
  <HomeIcons></HomeIcons>
  <HomeRecommand :recommandList="recommandList"></HomeRecommand>
</div>
</template>

<script>
import Header from '../components/Header'
import HomeSwiper from './children/Swiper'
import HomeIcons from './children/Icons'
import HomeRecommand from './children/Recommand'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    Header,
    HomeSwiper,
    HomeIcons,
    HomeRecommand
  },
  data () {
    return {
      recommandList: '',
      banner: ''
    }
  },
  methods: {
    getRecommand () {
      return axios.get('http://localhost:3000/personalized')
    },
    getBanner () {
      return axios.get('http://localhost:3000/banner')
    },
    getHomeInfo () {
      axios.all([this.getRecommand(), this.getBanner()])
        .then(axios.spread((res1, res2) => {
          this.getHomeInfoSucc(res1, res2)
        }))
    },
    getHomeInfoSucc (res1, res2) {
      res1 = res1.data
      res2 = res2.data
      this.recommandList = res1.result
      this.banner = res2.banners
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style>

</style>
