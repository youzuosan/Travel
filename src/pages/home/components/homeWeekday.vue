<template>
  <div class="wrap">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list"
        :key=item.id
      >
        <div class="imgWrap">
          <img class="item-img" :src=item.imgUrl />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-inner">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default{
  name: 'homeWeekday',
  props: {
    list: Array
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
        padding-bottom: 37.09%
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
