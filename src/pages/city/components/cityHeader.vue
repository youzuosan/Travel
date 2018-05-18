<template>
  <div class="cityHeader">
    <span>选择地址</span>
    <router-link to="/">
      <div class="iconfont return-sty">&#xe624;</div>
    </router-link>
  </div>
</template>
<script>
export default{
  name: 'cityHeader'
}
</script>
<style lang="stylus" scoped>
  @import "~styles/var.styl"
  .cityHeader
    overflow: hidden
    position: relative
    height: $headerHeight
    line-height: $headerHeight
    font-size: .32rem
    text-align: center
    color: #fff
    background-color: $bgColor
    .return-sty
      position: absolute
      top: 0
      left: 0
      width: .8rem
      height: $headerHeight
      line-height: $headerHeight
      color: #fff
</style>
