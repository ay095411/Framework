<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide v-for="(item,index) in swiperList" :key="index">
        <img :src="item" alt="" class="swiper-img">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
  export default {
    name:'HomeSwiper',
    data() {
      return {
        swiperList:['http://img1.qunarzz.com/piao/fusion/1809/31/da037478f37cf202.jpg_750x200_a02cf862.jpg',
        'http://img1.qunarzz.com/piao/fusion/1809/c6/2467595fffc3b302.jpg_750x200_cca13d51.jpg',
        'http://img1.qunarzz.com/piao/fusion/1809/ff/1bf7d3a4f6591002.jpg_750x200_40809f2a.jpg',
        'http://img1.qunarzz.com/piao/fusion/1811/1b/4143c7e0bfe78d02.jpg_750x200_5a220f6e.jpg'
        ],
        swiperOption: {
          pagination:'.swiper-pagination',
          loop:true
        }
      }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.swiper
      }
    },
    mounted() {
      console.log('this is current swiper instance object', this.swiper)
      this.swiper.slideTo(3, 1000, false)
    }
  }
</script>
<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active{background:#fff;}
.wrapper{width:100%;height:0;overflow:hidden;padding-bottom:27%;background:#eee;}
.swiper-img{width:100%;}
</style>