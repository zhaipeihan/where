<template>
    <div class='wrapper'>
        <swiper :options="swiperOption">
            <swiper-slide v-for="item in swiperList" :key='item.id'>
                <img class='swiper-img' :src='item.imgUrl'/>
            </swiper-slide>
            <div class='swiper-pagination'  slot="pagination"></div>
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
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/26/92e2470b26c00002.jpg_750x200_233f7f2b.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #ffffff
.wrapper {
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 26.67%;
    background: #eeeeee;

    .swiper-img {
        width: 100%;
    }
}
</style>
