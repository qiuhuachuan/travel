<template>
  <div class="icons">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.iconUrl" />
          </div>
          <p class="icon-desc">{{ item.content }}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [
        {
          id: '001',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          content: '景点门票景点门票景点门票景点门票'
        },
        {
          id: '002',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          content: '深圳必游'
        },
        {
          id: '003',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/4d/a1eda1a2b8414302.png',
          content: '夜场狂欢'
        },
        {
          id: '004',
          iconUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/815c90e59498644296e340c815e1269a.png',
          content: '世界之窗'
        },
        {
          id: '005',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          content: '一日游'
        },
        {
          id: '006',
          iconUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/cba147cf6cfcea7109d0bff6aac6f626.png',
          content: '深圳动物园'
        },
        {
          id: '007',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
          content: '泡温泉'
        },
        {
          id: '008',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          content: '东部华侨城'
        },
        {
          id: '009',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          content: '高空观景'
        },
        {
          id: '010',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png',
          content: '玩转长隆'
        }
      ],
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        }
      }
    }
  },
  computed: {
    pages () {
      const pagesList = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pagesList[page]) {
          pagesList[page] = []
        }
        pagesList[page].push(item)
      })
      return pagesList
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~@/assets/styles/mixins.styl'
.icons >>> swiper-container {
  height: 0;
  padding-bottom: 50%;
}

.icon {
  position: relative;
  overflow: hidden;
  float: left;
  width: 25%;
  height: 0;
  padding-bottom: 25%;
}

.icon-img {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0.44rem;
  box-sizing: border-box;
  padding: 0.1rem;
}

.icon-img-content {
  display: block;
  margin: 0 auto;
  height: 100%;
}

.icon-desc {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 0.44rem;
  line-height: 0.44rem;
  text-align: center;
  color: #333;
  ellipsis();
}
</style>
