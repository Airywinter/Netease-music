<template>
  <div class="icons">
    <div class="icon" v-for="item of iconList" :key="item.id">
        <img class="svg" :src="item.iconUrl">
        <span>{{item.content}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data: function () {
    return {
      iconList: [{
        id: '001',
        iconUrl: 'static/音乐_music215.svg',
        content: '私人FM'
      }, {
        id: '002',
        iconUrl: 'static/音乐_music215.svg',
        content: '每日推荐'
      }, {
        id: '003',
        iconUrl: 'static/音乐_music215.svg',
        content: '歌单'
      }, {
        id: '004',
        iconUrl: 'static/音乐_music215.svg',
        content: '排行榜'
      }]
    }
  }
}
</script>

<style lang="scss">
.icons {
  height: 1.5rem;
  border-bottom: 1px solid #F0F0F0;
  .icon {
    box-sizing: border-box;
    padding: 0.2rem;
    float: left;
    width: 25%;
    height: 100%;
    text-align: center;
    font-size: 0.1rem;
    color: black;
    .svg {
      margin-bottom: 0.1rem;
      width: 80%;
      height: 80%;
    }
  }
}
</style>
