<template>
    <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide><img class="swiper-img" src="http://img1.qunarzz.com/sight/source/1507/d9/2ddc7652fdba16.jpg_r_640x214_5e62f1a3.jpg" alt=""></swiper-slide>
    <swiper-slide><img class="swiper-img" src="http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg"></swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination',
          checkable: true
        }
      }
    }
  },
  computed: {
    swiper () {
      return this.$refs.mySwiper.$swiper
    }
  },
  mounted () {
    this.swiper.slideTo(3, 1000, false)
  }
}
</script>

<style lang='stylus' scoped>
  .wrapper
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 37.68%
    .swiper-img
      width: 100%
</style>
