<template>
  <div class="citySearch">
    <input class="search" type="search" placeholder="请输入城市/拼音" />
  </div>
</template>
<script>
export default{
  name: 'citySearch'
}
</script>
<style lang="stylus" scoped>
  @import "~styles/var.styl"
  .citySearch
    height: .72rem
    background: $bgColor
    padding: 0 .1rem
    .search
      box-sizing: border-box
      width: 100%
      height: .62rem
      line-height: .62rem
      text-align: center
      padding: 0 .1rem
      border-radius: .06rem
      color: #666
</style>
