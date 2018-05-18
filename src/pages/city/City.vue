<template>
  <div>
    <cityHeader></cityHeader>
    <citySearch></citySearch>
    <cityList></cityList>
    <ZM></ZM>
  </div>
</template>
<script>
import cityHeader from '@/pages/city/components/cityHeader'
import citySearch from '@/pages/city/components/citySearch'
import cityList from '@/pages/city/components/cityList'
import ZM from '@/pages/city/components/ziMu'
export default{
  name: 'City',
  components: {
    cityHeader,
    citySearch,
    cityList,
    ZM
  }
}
</script>
<style lang="stylus" scoped></style>
