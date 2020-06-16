<script>
export default {}
</script>

<style lang="scss">
/*每个页面公共css */
.common-page-container {
  // 每个页面
  min-width: 100vw;
  min-height: 100vh;
  background-color: #f5f5f5;
  overflow-x: hidden;
  > view {
    width: 100%;
    background-color: #fff;
    box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.2);
    border-radius: 8px;
    padding: 12px;
  }
}
.common-container {
  // 每个功能模块盒子
  width: 100%;
  background-color: #fff;
  box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.2);
  border-radius: 8px;
  padding: 12px;
}
</style>
