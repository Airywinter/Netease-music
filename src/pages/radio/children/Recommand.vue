<template>
  <div class="radio-recommand">
    <p>
      <span class="title">今日优选</span>
      <span class="arrow">></span>
    </p>
    <div class="radio-recommand-wrapper">
        <div class="radio-recommand-list" v-for="item of djRecommand" :key="item.id">
            <img class="radio-recommand-img" :src="item.picUrl">
            <div class="text">
              <p class="radio-recommand-name">{{item.name}}</p>
              <p class="radio-recommand-text">{{item.rcmdtext}}</p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RadioRecommand',
  props: ['djRecommand']
}
</script>

<style lang="scss">
.radio-recommand {
    padding-top: 1.7rem;
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
    .radio-recommand-wrapper {
        .radio-recommand-list {
            margin-bottom: 0.1rem;
            height: 2rem;
            .radio-recommand-img {
                float: left;
                width: 2rem;
                height: 100%;
            }
            .text {
                box-sizing: border-box;
                padding-top: 0.3rem;
                border-bottom: 1px solid rgb(231, 228, 228);
                margin-left: 2.3rem;
                height: 2rem;
            .radio-recommand-name {
                margin-bottom: 0.3rem;
                font-size: 0.3rem;
                font-weight: 500;
                color: black;
            }
            .radio-recommand-text {
               font-size: 0.2rem;
            }
        }
      } 
    }
}
</style>
