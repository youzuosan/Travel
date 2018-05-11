<template>
  <div class="slider">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of sliderList" :key="item.id" >
        <img class="sliderImg" :src="item.src" />
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
      },
      sliderList: [
        {
          id: 1,
          src: 'http://img1.qunarzz.com/piao/fusion/1804/15/9250dbc86a456302.jpg_750x200_b423f532.jpg'
        }, {
          id: 2,
          src: 'http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg'
        }, {
          id: 3,
          src: 'http://img1.qunarzz.com/piao/fusion/1803/43/94da80bae59dfb02.jpg_750x200_00b1cc66.jpg'
        }, {
          id: 4,
          src: 'http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg'
        }, {
          id: 5,
          src: 'http://img1.qunarzz.com/piao/fusion/1803/43/94da80bae59dfb02.jpg_750x200_00b1cc66.jpg'
        }, {
          id: 6,
          src: 'http://img1.qunarzz.com/piao/fusion/1803/26/92e2470b26c00002.jpg_750x200_233f7f2b.jpg'
        }
      ]
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
