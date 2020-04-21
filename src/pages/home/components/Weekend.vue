<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-botttom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
          title: '北京赏花好地方',
          desc: '乱花渐欲迷人眼，京城赏花大搜索'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
          title: '京城周末撒欢',
          desc: '在帝都过周末，不仅仅是城中游！'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
          title: '北京赏花好地方',
          desc: '乱花渐欲迷人眼，京城赏花大搜索'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
          title: '京城周末撒欢',
          desc: '在帝都过周末，不仅仅是城中游！'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
          title: '北京赏花好地方',
          desc: '乱花渐欲迷人眼，京城赏花大搜索'
        },
        {
          id: '0006',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
          title: '京城周末撒欢',
          desc: '在帝都过周末，不仅仅是城中游！'
        },
        {
          id: '0007',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
          title: '北京赏花好地方',
          desc: '乱花渐欲迷人眼，京城赏花大搜索'
        },
        {
          id: '0008',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
          title: '京城周末撒欢',
          desc: '在帝都过周末，不仅仅是城中游！'
        }
      ]
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~@/assets/styles/mixins.styl'

.recommend-title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem
}
.item-img-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 33.5%;
}

.item-img {
  width: 100%;
}

.item-info {
  padding: 0.06rem 0.1rem 0.2rem;
}

.item-title {
  line-height: 0.54rem;
  font-size: 0.28rem;
  ellipsis();
}

.item-desc {
  line-height: 0.4rem;
  font-size: 0.24rem;
  color: #ccc;
  ellipsis();
}
</style>
