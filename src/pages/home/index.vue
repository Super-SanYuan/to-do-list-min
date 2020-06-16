<template>
  <view class="home-page-container common-page-container">
    <view class="header-container">
      <view class="logo"></view>
      <input type="text" />
      <button>添加今日代办</button>
    </view>
    <ecCanvas />
    <view class="main-container">
      <view class="title">
        <text>今日代办:</text>
      </view>
      <view v-for="item in toDoList" class="items">
        <view :key="item.id" class="item">{{ item.text }}</view>
      </view>
    </view>
  </view>
</template>

<script>
import ecCanvas from '../../../components/ec-canvas/ec-canvas'
export default {
  data() {
    return {
      toDoList: [
        {
          id: 1,
          text: '洗头发',
        },
        {
          id: 2,
          text: '四物汤',
        },
      ],
    }
  },
  components: {
    ecCanvas
  },
  onLoad() {},
  methods: {},
}
</script>

<style lang="scss">
@import 'app.scss';
.home-page-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  .header-container {
    height: 90upx;
    display: flex;
    input {
      height: 100%;
      border: 1px solid red;
    }
    color: red;
    button {
      color: $app-color-primary;
    }
  }
  .main-container {
    background-color: #fff;
    margin-top: 10px;
    .title {
      font-size: 16px;
      font-weight: 700;
    }
    .items {
      display: flex;
      justify-content: center;
      .item {
        margin: 4px 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
    }
  }
}
</style>
