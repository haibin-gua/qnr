<template>
  <div class="icons">
    <swiper>
     <swiper-slide v-for="(page,index) of pages" :key="index">
      <div class="icon" v-for="item of page" :key="item.id">
      <div class="icon_img">
        <img class="icon_imgcontent" :src="item.imgUrl">
      </div>
        <p class="icon-desc">{{item.desc}}</p>
      </div>
    </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name:'HomeIcons',
  data () {
    return{
      iconsList:[{
        id:'0001',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc:'景点门票'
      },{
        id:'0002',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/48/cb72b99b71974c02.png',
        desc:'生活休闲'
      },{
        id:'0003',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        desc:'亲子游'
      },{
        id:'0004',
        imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc:'自然风光'
      },{
        id:'0005',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/3a/754b47f658e9c602.png',
        desc:'桃花冲漂流'
      },{
        id:'0006',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc:'景点门票'
      },{
        id:'0007',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/48/cb72b99b71974c02.png',
        desc:'生活休闲'
      },{
        id:'0008',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        desc:'亲子游'
      },{
        id:'0009',
        imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc:'自然风光'
      },{
        id:'0010',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/3a/754b47f658e9c602.png',
        desc:'桃花冲漂流'
      }]
    }
  },
    computed:{
      pages () {
        const pages = []
        this.iconsList.forEach((item,index) => {
          const page = Math.floor(index / 8)
          if(!pages[page]) {
            pages[page] = []
          }
          pages[page].push(item)
        })
        return pages
      }
    }
    }
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/varibles.styl'
@import '../../../assets/styles/mixins.styl'
  .icons >>> .swiper-container
   height:0
   padding-bottom:50%
   .icon
    position :relative
    overflow :hidden
    width:25%
    height:0
    float:left
    padding-bottom:25%
    .icon_img{
      position :absolute
      top:0
      left:0
      right:0
      bottom :.44rem
      box-sizing :border-box
      padding:.1rem
    }
    .icon_imgcontent{
      display :block
      margin:0 auto
      height:100%
    }
    .icon-desc{
      position :absolute
      left:0
      right:0
      bottom:0
      height:.44rem
      line-height :.44rem
      color:$darkTextColor
      text-align :center
      ellipsis()
    }
</style>
