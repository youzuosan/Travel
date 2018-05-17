<template>
  <div class="slider">
    <swiper :options="swiperOption" v-if="show">
      <!-- slides -->
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="sliderImg" :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'indexSlider',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: '2000'
      }
    }
  },
  props: {
    list: Array
  },
  computed: {
    show () {
      return this.list.length
    }
  }
}
</script>
<style lang="stylus" scoped>
  .slider >>> .swiper-pagination-bullet-active
    background: #fff
  .slider
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 26%
    background: #eee
    .sliderImg
      width: 100%
      height: 100%
</style>
