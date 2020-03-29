<template>
  <div>
    <div class="title">周末去哪儿</div>
      <ul>
        <li class="item border-bottom" v-for="item of list" :key="item.id">
            <img class="item-img" :src='item.imgUrl'>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
          </div>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  name:'HomeWeekend',
  props:{
    list:Array
  }
}
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/mixins.styl'
  .title
    margin-top:.2rem
    line-height :.8rem
    background :#eee
    text-indent .2rem
    padding-bottm:33.9%
    .item-img
     width:100%
  .item-info
    padding:.1rem
    .item-title
      ellipsis()
      line-height :.54rem
      font-size :.32rem
    .item-desc
      line-height :.44rem
      color:#CCCCCC
      ellipsis()
</style>
