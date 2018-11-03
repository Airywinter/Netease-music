<template>
<div class="home-recommand">
  <p>
    <span class="title">推荐歌单</span>
    <span class="arrow">></span>
  </p>
  <div class="recommand-wrapper">
    <div class="recommand-list" v-for="item of recommandList" :key="item.id">
      <img class="recommand-img" :src="item.picUrl">
      <span class="recommand-name">{{item.name}}</span>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'HomeRecommand',
  props: ['recommandList']
}
</script>

<style lang="scss">
.title {
    margin: 0.2rem 0 0.2rem 0.2rem;
    height: 0.7rem;
    line-height: 0.7rem;
    font-size: 0.3rem;
    font-weight: 500;
    color: black;
}
.arrow {
    font-size: 0.3rem;
    color: gray;
}
.recommand-wrapper {
    .recommand-list {
        float: left;
        margin-bottom: 0.2rem;
        margin-left: 1%;
        width: 32%;
        height: 3rem;
        .recommand-img {
            width: 100%;
        }
        .recommand-name {
          font-size: 0.15rem;
          color: black;
        }
  }
}

</style>
