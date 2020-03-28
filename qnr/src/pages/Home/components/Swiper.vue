<template>
  <div class="wrapper">
  <swiper :options="swiperOptions">
      <swiper-slide v-for="item of swiperList">
        <img class="swiper-img" :src="item.imgUrl" :key="item.id">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    </div>
</template>

<script>
 export default {
   name:'HomeSwiper',
   data () {
     return{
       swiperOptions:{
         pagination:'.swiper-pagination',
         loop:true
       },
       swiperList:[{
         id: '0001',
         imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/86ca4dc2777b997607e97eb8471dcafd.jpg_890x330_0eee7728.jpg'
       },
       {
         id: '0002',
         imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/8216fd250c35366befc35f6353f934b9.jpg_890x330_9062b3ba.jpg'
       }]
     }
   }
 }
</script>

<style lang="stylus" scoped>
  .wrapper >>>.swiper-pagination-bullet-active
   background :#fff
  .swiper-img
   width:100%
</style>
