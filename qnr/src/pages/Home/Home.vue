<template>
  <div>
    <home-headr></home-headr>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    </div>
</template>

<script>
 import HomeHeadr from './components/Header.vue'
 import HomeSwiper from './components/Swiper.vue'
 import HomeIcons from './components/Icons.vue'
 export default {
   name:'Home',
   components:{
     HomeHeadr,
     HomeSwiper,
     HomeIcons
   }
 }
</script>

<style>
</style>
