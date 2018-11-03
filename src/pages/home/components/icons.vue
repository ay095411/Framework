<template>
  <div class="icons">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon">
          <div class="icon-image" v-for="(item,index) of page" :key="index">
            <img :src="item.images" class="icon-image-content" alt="">
            <p class="icon-desc">{{item.desc}}</p>
          </div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination"
      },
      iconList: [
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
          desc: "一日游"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "郑州必游"
        },
        {
          images:
            "https://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png",
          desc: "打卡圣地"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1803/f5/a963333e1fa802.png",
          desc: "当地好玩"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png",
          desc: "动物园"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png",
          desc: "名胜古迹"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png",
          desc: "泡温泉"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png",
          desc: "主题乐园"
        },
        {
          images:
            "http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png",
          desc: "全部玩乐"
        }
      ]
    };
  },
  computed: {
    pages() {
      const pages = [];
      this.iconList.forEach((item,index) => {
        const page = Math.floor(index / 8);
        if(!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages;
    }
  }
};
</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';
.icons >>> .swiper-pagination-bullet-active {
  background: rgba(0, 175, 190, 0.8);
}

.icons >>> .swiper-container {
  width: 100%;
  height: 0;
  padding-bottom: 50%;
}

.icon {
  position: relative;
  width: 100%;
  padding-bottom: 25%;
}

.icon-image {
  width: 25%;
  padding: 0.1rem;
  float: left;
}

.icon-image-content {
  width: 52px;
  height: 25%;
  display: block;
  margin: 0 auto;
}

.icon-desc {
  position: absolut;
  left: 0;
  right: 0;
  bottom: 0;
  height: 0.44rem;
  line-height: 0.44rem;
  color: $darkTextColor;
  text-align: center;
  ellipsis()
}
</style>
