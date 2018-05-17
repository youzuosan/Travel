<template>
  <div class="recomWrap">
    <div class="title"><span class="iconfont">&#xe62d;</span>猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of list"
        :key=item.id
      >
        <img class="item-img" :src=item.imgUrl />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-inner">{{item.desc}}</p>
          <p class="item-charge">
            <span class="money">￥88</span>起
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default{
  name: 'homeRecommend',
  props: {
    list: Array
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
