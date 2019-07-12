<template>
  <div>
    <div class="box"></div>
    <van-button type="default">默认按钮</van-button>
    <van-button type="primary">主要按钮</van-button>
    <van-button type="info">信息按钮</van-button>
    <van-button type="warning">警告按钮</van-button>
    <van-button type="danger">危险按钮</van-button>
  </div>
</template>

<script>
export default {
  name: 'HomeIndex',
  data () {
    return {}
  },
  components: {

  }
}
</script>

<style lang="less" scoped>
.box {
  width: 375px;
  height: 100px;
  background-color: red;
}
</style>
