<template>
<div class="list" ref="wrapper">
  <div>
    <div class="area">
      <div class="title border-topbottom">您的位置</div>
      <div class="buttonList">
        <div class="buttonWrap">
          <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">热门城市</div>
      <div class="buttonList">
        <div class="buttonWrap">
          <div class="button">北京</div>
        </div>
        <div class="buttonWrap">
          <div class="button">北京</div>
        </div>
        <div class="buttonWrap">
          <div class="button">北京</div>
        </div>
        <div class="buttonWrap">
          <div class="button">北京</div>
        </div>
        <div class="buttonWrap">
          <div class="button">北京</div>
        </div>
        <div class="buttonWrap">
          <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="itemList">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="itemList">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="itemList">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
  </div>
</div>
</template>
<script>
import BScroll from 'better-scroll'
export default{
  name: 'cityList',
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/var.styl"
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .border-bottom
    &:before
      border-color: #ccc
  .list
    overflow: hidden
    position: absolute
    top: 1.58rem
    bottom: 0
    left: 0
    right: 0
    .title
      line-height: .54rem
      font-size: .26rem
      background: #eee
      padding-left: .2rem
      color: #666
    .buttonList
      padding: .1rem  .6rem .1rem .1rem
      overflow: hidden
      .buttonWrap
        float: left
        width: 33.33%
        .button
          margin: .1rem
          padding: .1rem 0
          text-align: center
          border: .02rem solid #ccc
          border-radius: .06rem
    .itemList
      .item
        line-height: .76rem
        padding-left: .2rem
</style>
