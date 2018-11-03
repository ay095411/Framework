<template>
  <div>
    <HomeHeader></HomeHeader>
    <HomeSwiper></HomeSwiper>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/swiper'
  export default {
    name:'Home',
    components: {
      HomeHeader,
      HomeSwiper
    },
    data() {
      return {
        
      }
    }
  }
</script>
<style scoped>

</style>
