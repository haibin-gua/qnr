<template>
  <div class="search">
    <input class="search-input" tupe="text" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name:'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/varibles.styl'
  .search
    height:.72rem
    padding:0 .1rem
    background :$bgColor
    .search-input
      box-sizing :border-box
      text-align :center
      width:100%
      padding:0 .1rem
      height:.62rem
      line-height :.62rem
      border-radius .06rem
      color:#666
</style>
