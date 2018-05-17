<template>
  <div class="icon">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(pages, index) of pages" :key="index">
        <div class="iconList" v-for="item of pages" :key="item.id">
          <div class="iconImgW">
            <img  class="iconImg" :src="item.imgUrl" />
          </div>
          <p class="iconTitle">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default{
  name: 'homeIcon',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: false
      }
    }
  },
  props: {
    list: Array
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .icon >>> .swiper-slide
    width: 100%
    padding-bottom: 50%
    height: 0
  .icon
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .iconList
      position: relative
      overflow: hidden
      width: 25%
      height: 0
      padding-bottom: 25%
      float: left
      .iconImgW
        position: absolute
        top: 0
        right: 0
        left: 0
        bottom: .44rem
        border-sizing: border-box
        padding: .1rem
        .iconImg
          height: 100%
          display: block
          margin: 0 auto
      .iconTitle
        position:absolute
        right: 0
        left: 0
        bottom: 0
        line-height: .44rem
        height: .44rem
        text-align: center
        ellipsis()
</style>
