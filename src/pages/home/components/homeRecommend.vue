<template>
  <div class="recomWrap">
    <div class="title"><span class="iconfont">&#xe62d;</span>猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList"
        :key=item.id
      >
        <img class="item-img" :src=item.imgUrl />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-inner">{{item.inner}}</p>
          <p class="item-charge">
            <span class="money">￥{{item.money}}</span>起
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default{
  name: 'homeRecommend',
  data () {
    return {
      recommendList: [{
        id: 1,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/c7/c74a66ec65491fc2a3.img.jpg_200x200_57fd010d.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩',
        money: '88'
      }, {
        id: 2,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/c7/c74a66ec65491fc2a3.img.jpg_200x200_57fd010d.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩',
        money: '88'
      }, {
        id: 3,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/c7/c74a66ec65491fc2a3.img.jpg_200x200_57fd010d.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩',
        money: '88'
      }, {
        id: 4,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/c7/c74a66ec65491fc2a3.img.jpg_200x200_57fd010d.jpg',
        title: '青岛东方影都万达乐园',
        inner: '好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩好玩',
        money: '88'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .recomWrap
    .title
      margin-top: .1rem
      height: .9rem
      line-height: .9rem
      background-color: #e6e6e6
      .iconfont
        color: red
        padding-left: .2rem
    .item
      overflow: hidden
      display: flex
      height: 1.9rem
      .item-img
        weidth: 1.7rem
        height: 1.7rem
        padding: .1rem
      .item-info
        flex: 1
        padding: .1rem
        min-width: 0
        .item-title
          line-height: .54rem
          font-size: .4rem
          ellipsis()
        .item-inner
          line-height: .4rem
          color: #ccc
          ellipsis()
        .item-charge
          line-height: .5rem
          margin-top: .2rem
          .money
            color: #ff8300
            font-size: .4rem
</style>
