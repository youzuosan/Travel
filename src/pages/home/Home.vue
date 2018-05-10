<template>
  <div>
    <home-header></home-header>
    <indexSlider></indexSlider>
  </div>
</template>

<script>
import homeHeader from '@/pages/home/components/homeHeader'
import indexSlider from '@/pages/home/components/homeSlider'
export default {
  name: 'Home',
  components: {
    homeHeader,
    indexSlider
  }
}
</script>

<style></style>
