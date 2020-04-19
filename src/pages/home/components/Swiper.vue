<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" v-bind:src="item.imgUrl" />
      </swiper-slide>
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
        loop: true,
        autoplay: true,
        speed: 2000,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        }
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/80/29eaf59b380bef97acacba8a8f6efd2a.water.jpg_600x330_76f8cfee.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/88/880775ea761f2c1390.water.jpg_600x330_1fc3551a.jpg'
        }
      ]
    }
  }
}
</script>

<style lang='stylus' scoped>
.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 55%;
  background: #eee;
}

.swiper-img {
  width: 100%;
}

.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}
</style>
