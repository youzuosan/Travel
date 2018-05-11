<template>
  <div>
    <home-header></home-header>
    <indexSlider></indexSlider>
    <homeIcon></homeIcon>
  </div>
</template>

<script>
import homeHeader from '@/pages/home/components/homeHeader'
import indexSlider from '@/pages/home/components/homeSlider'
import homeIcon from '@/pages/home/components/homeIcon'
export default {
  name: 'Home',
  components: {
    homeHeader,
    indexSlider,
    homeIcon
  }
}
</script>

<style></style>
