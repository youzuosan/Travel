<template>
  <div class="header">
     <div class="header-left">
       <div class="iconfont return-sty">&#xe624;</div>
     </div>
     <div class="header-input">
       <span class="iconfont input-sty">&#xe632;</span>
       输入城市景点/游玩主题
     </div>
     <div class="header-right">城市<span class="iconfont">&#xe64a;</span></div>
  </div>
</template>

<script>
export default {
  name: 'homeHeader'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/var.styl"
  .header
    line-height: .86rem
    display: flex
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .return-sty
        font-size: .4rem
        text-align: center
    .header-right
      width: 1.24rem
      float: right
      text-align: center
    .header-input
      flex: 1
      background: #fff
      color:#eff4f8
      border-radius: .1rem
      height: .64rem
      line-height: .64rem
      margin-left: .2rem
      margin-top: .12rem
      .input-sty
        padding-left: .2rem
</style>
