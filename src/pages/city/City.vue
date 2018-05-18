<template>
  <div>
    <cityHeader></cityHeader>
    <citySearch></citySearch>
  </div>
</template>
<script>
import cityHeader from '@/pages/city/components/cityHeader'
import citySearch from '@/pages/city/components/citySearch'
export default{
  name: 'City',
  components: {
    cityHeader,
    citySearch
  }
}
</script>
<style lang="stylus" scoped></style>
