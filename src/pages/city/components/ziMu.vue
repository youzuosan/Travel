<template>
  <ul class="list">
    <li class="item">A</li>
    <li class="item">B</li>
    <li class="item">C</li>
    <li class="item">D</li>
    <li class="item">E</li>
    <li class="item">F</li>
    <li class="item">G</li>
    <li class="item">H</li>
    <li class="item">I</li>
    <li class="item">J</li>
    <li class="item">K</li>
    <li class="item">L</li>
    <li class="item">M</li>
    <li class="item">N</li>
    <li class="item">O</li>
    <li class="item">P</li>
    <li class="item">Q</li>
  </ul>
</template>
<script>
export default{
  name: 'ZM'
}
</script>
<style lang="stylus" scoped>
  @import"~styles/var.styl"
  .list
    display: flex
    flex-direction: column
    justify-content: center
    position: absolute
    top: 1.58rem
    right: 0
    bottom: 0
    width: .4rem
    .item
      text-align: center
      color: $bgColor
</style>
