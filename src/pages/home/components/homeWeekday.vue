<template>
  <div class="wrap">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList"
        :key=item.id
      >
        <div class="imgWrap">
          <img class="item-img" :src=item.imgUrl />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-inner">{{item.inner}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default{
  name: 'homeWeekday',
  data () {
    return {
      recommendList: [{
        id: 1,
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ef/815eec316c47c4.jpg_r_640x214_5bf7f999.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩'
      }, {
        id: 2,
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/87/b46b43303b585c.jpg_r_640x214_af2aa659.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩'
      }, {
        id: 3,
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ef/815eec316c47c4.jpg_r_640x214_5bf7f999.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩'
      }, {
        id: 4,
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/87/b46b43303b585c.jpg_r_640x214_af2aa659.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .wrap
    .title
      padding-left: .2rem
      margin-top: .1rem
      height: .9rem
      line-height: .9rem
      background-color: #e6e6e6
    .item
      overflow: hidden
      .imgWrap
        overflow: hidden
        height: 0
        padding-bottom: 33.9%
        .item-img
          padding: .1rem
          width: 100%
      .item-info
        padding: .1rem
        min-width: 0
        .item-title
          line-height: .48rem
          font-size: .24rem
          ellipsis()
        .item-inner
          line-height: .48rem
          font-size: .2rem
          color: #616161
          ellipsis()
</style>
