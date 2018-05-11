<template>
  <div class="icon">
    <swiper>
      <swiper-slide v-for="(pages, index) of pages" :key="index">
        <div class="iconList" v-for="item of pages" :key="item.id">
          <div class="iconImgW">
            <img  class="iconImg" :src="item.url" />
          </div>
          <p class="iconTitle">{{item.title}}</p>
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
      iconList: [{
        id: 1,
        url: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: 2,
        url: 'https://imgs.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        title: '必游榜单'
      }, {
        id: 3,
        url: 'https://imgs.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
        title: '自然风光'
      }, {
        id: 4,
        url: 'https://imgs.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        title: '游乐场'
      }, {
        id: 5,
        url: 'https://imgs.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        title: '趵突泉'
      }, {
        id: 6,
        url: 'https://imgs.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        title: '名胜古迹'
      }, {
        id: 7,
        url: 'https://imgs.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
        title: '大明湖'
      }, {
        id: 8,
        url: 'https://imgs.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        title: '七日游'
      }, {
        id: 9,
        url: 'https://imgs.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        title: '二日游'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
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
