<template>
  <div class="head-wrapper">
    <div class="head-top">
      <span class="iconfont icon1">&#xe67e;</span>
      <input class="input iconfont" :placeholder='icon'>
      <span class="iconfont icon2">&#xe680;</span>
    </div>
    <div id="head-bottom">
      <router-link to="/">
        <span class="head-bottom-left">个性推荐</span>
      </router-link>
      <router-link to="/radio">
        <span class="head-bottom-right">主播电台</span>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data: function () {
    return {
      icon: '\ue64d 音乐/视频/电台/用户'
    }
  }
}
</script>

<style lang="scss">
@import '~@/assets/styles/variables.scss';
.head-wrapper {
  position: fixed;
  z-index: 9999;
  width: 100%;
  height: 1.7rem;
  background-color: $background-color;
  .head-top {
    padding: 0.1rem;
    height: 0.7rem;
    line-height: 0.7rem;
    text-align:center;
    color: $font-color;
    .icon1 {
      float: left;
      font-size: 0.5rem;
    }
    .icon2 {
      float: right;
      font-size: 0.5rem;
    }
    .input {
      padding-left: 0.1rem;
      min-width: 5.5rem;
      height: 0.5rem;
      text-align: center;
      border-radius: 5rem;
      font-size: 0.3rem;
    }
  }
  #head-bottom {
    height: 0.8rem;
    line-height: 0.8rem;
    text-align: center;
    font-size: 0.3rem;
    .head-bottom-left {
      margin-right: 1rem;
      color: $font-color;
    }
    .head-bottom-right {
      color: $font-color;
    }
  }
}
</style>
