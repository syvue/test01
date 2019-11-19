<template>
    <div class="wrapper">
        <swiper :options="swiperOption" >
            <!-- slides -->
            <swiper-slide v-for='item of swiperList' :key='item.id'>
                <img class='swiper-img' :src='item.imgUrl' />
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 5000
      },
      swiperList: [{
        id: '001',
        imgUrl: require('images/swiper01.jpg')
      }, {
        id: '002',
        imgUrl: require('images/swiper02.jpg')
      }, {
        id: '003',
        imgUrl: require('images/swiper03.jpg')
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 26.66%
    .swiper-img
      width 100%
</style>
