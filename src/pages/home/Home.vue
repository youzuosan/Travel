<template>
  <div>
    <home-header :city="city"></home-header>
    <indexSlider :list="swiperList"></indexSlider>
    <homeIcon :list="iconList"></homeIcon>
    <homeRecommend :list="recommendList"></homeRecommend>
    <homeWeekday :list="weekendList"></homeWeekday>
  </div>
</template>

<script>
import homeHeader from '@/pages/home/components/homeHeader'
import indexSlider from '@/pages/home/components/homeSlider'
import homeIcon from '@/pages/home/components/homeIcon'
import homeRecommend from '@/pages/home/components/homeRecommend'
import homeWeekday from '@/pages/home/components/homeWeekday'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    homeHeader,
    indexSlider,
    homeIcon,
    homeRecommend,
    homeWeekday
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
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
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style></style>
