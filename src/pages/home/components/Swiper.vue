<template>
  <swiper :options="swiperOption" class="swiper">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        autoplay: true,
        speed: 4000,
        grabCursor: true,
        pagination: '.swiper-pagination',
        paginationClickable: true
      },
      swiperList: [{
        id: '001',
        imgUrl: 'http://p1.music.126.net/o8Lb7goshWNeiGZNtPatpg==/109951163626308990.jpg'
      }, {
        id: '002',
        imgUrl: 'http://p1.music.126.net/srXzyd56hrb3YXtt5Aplaw==/109951163630511154.jpg'
      }, {
        id: '003',
        imgUrl: 'http://p1.music.126.net/792N-RbDeb3aTCFl_qp5qA==/109951163625124943.jpg'
      }, {
        id: '004',
        imgUrl: 'http://p1.music.126.net/85wWRH5Nqq_imCHdzsvcUA==/109951163631817985.jpg'
      }, {
        id: '005',
        imgUrl: 'http://p1.music.126.net/yg_1jApSQdYjhLJfGpe-0g==/109951163631515001.jpg'
      }]
    }
  }
}
</script>

<style lang="scss">
@import '../../../assets/styles/variables.scss';
  .swiper-img {
    width: 100%;
  }
  .swiper-pagination-bullet {
    background-color: $background-color !important;
  }
</style>
