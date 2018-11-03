<template>
  <div>
    <RadioHeader></RadioHeader>
    <RadioRecommand :djRecommand="djRecommand"></RadioRecommand>
  </div>
</template>

<script>
import RadioHeader from '../components/Header'
import RadioRecommand from './children/Recommand'
import axios from 'axios'
export default {
  name: 'Radio',
  components: {
    RadioHeader,
    RadioRecommand
  },
  data () {
    return {
      djRecommand: ''
    }
  },
  methods: {
    getRadioInfo () {
      axios.get('http://localhost:3000/dj/recommend')
        .then((res) => {
          res = res.data
          this.djRecommand = res.djRadios
        })
    }
  },
  mounted () {
    this.getRadioInfo()
  }
}
</script>

<style lang="scss">

</style>
