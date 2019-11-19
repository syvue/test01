<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for='(page, index) of pages' :key='index'>
                <div class="icon" v-for="item of page" :key="item.id" >
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgUrl" />
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        autoplay: false
      },
      iconList: [{
        id: '001',
        imgUrl: require('images/icon01.png'),
        desc: '景点门票'
      }, {
        id: '002',
        imgUrl: require('images/icon02.png'),
        desc: '景点门票'
      }, {
        id: '003',
        imgUrl: require('images/icon03.png'),
        desc: '景点门票'
      }, {
        id: '004',
        imgUrl: require('images/icon04.png'),
        desc: '景点门票'
      }, {
        id: '005',
        imgUrl: require('images/icon01.png'),
        desc: '景点门票'
      }, {
        id: '006',
        imgUrl: require('images/icon02.png'),
        desc: '景点门票'
      }, {
        id: '007',
        imgUrl: require('images/icon03.png'),
        desc: '景点门票'
      }, {
        id: '008',
        imgUrl: require('images/icon04.png'),
        desc: '景点门票'
      }, {
        id: '009',
        imgUrl: require('images/icon04.png'),
        desc: '景点门票'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
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
@import '~styles/varibles.styl';
     .icons >>> .swiper-container
       height 0
       padding-bottom 50%
       background #eee
     .icon
       overflow hidden
       float left
       width 25%
       height 0
       padding-bottom 25%
       position relative
       .icon-img
         position absolute
         top 0
         left 0
         right 0
         bottom .44rem
         box-sizing border-box
         .icon-img-content
           display block
           margin 0 auto
           height 100%
        .icon-desc
          position absolute
          left 0
          right 0
          bottom 0
          height .44rem
          line-height .44rem
          text-align center
          ellipsis()
</style>
