<template>
  <view class="common-page-container circle-page-container">
    <view class="circle-swiper">
      <swiper
        :autoplay="true"
        :indicator-dots="true"
        :circular="true"
        indicator-color="rgba(0, 255, 0, .3)"
        indicator-active-color="rgb(255, 190, 180)"
      >
        <template v-for="item in bannerList">
          <swiper-item class="swiper-item" :key="item.id">{{ item.text }}</swiper-item>
        </template>
      </swiper>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      bannerList: [
        {
          id: 1,
          text: '死生契阔，与子成说。 执子之手，与子偕老',
        },
        {
          id: 2,
          text: '青青子衿，悠悠我心，纵我不往，子宁不嗣音',
        },
        {
          id: 3,
          text: '今夕何夕，见此良人。子兮子兮，如此良人何',
        },
      ],
    }
  },
  onLoad() {},
  methods: {},
}
</script>

<style lang="scss">
@import 'app.scss';
.circle-page-container {
  .swiper-item {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
