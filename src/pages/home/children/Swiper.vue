<template>
  <swiper :options="swiperOption" class="swiper">
    <!-- slides -->
    <swiper-slide v-for="item of banner" :key="item.targetId">
        <img class="swiper-img" :src="item.imageUrl">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: ['banner'],
  data: function () {
    return {
      swiperOption: {
        autoplay: true,
        speed: 4000,
        grabCursor: true,
        pagination: '.swiper-pagination',
        paginationClickable: true
      }
    }
  }
}
</script>

<style lang="scss">
@import '~@/assets/styles/variables.scss';
  .swiper-img {
    padding-top: 1.7rem;
    width: 100%;
  }
  .swiper-pagination-bullet {
    background-color: $background-color !important;
  }
</style>
