<template>
  <div>
    <home-header></home-header>
    <indexSlider></indexSlider>
    <homeIcon></homeIcon>
    <homeRecommend></homeRecommend>
    <homeWeekday></homeWeekday>
  </div>
</template>

<script>
import homeHeader from '@/pages/home/components/homeHeader'
import indexSlider from '@/pages/home/components/homeSlider'
import homeIcon from '@/pages/home/components/homeIcon'
import homeRecommend from '@/pages/home/components/homeRecommend'
import homeWeekday from '@/pages/home/components/homeWeekday'
export default {
  name: 'Home',
  components: {
    homeHeader,
    indexSlider,
    homeIcon,
    homeRecommend,
    homeWeekday
  }
}
</script>

<style></style>
