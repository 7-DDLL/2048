<template>
  
  <div class="home">
    <top-nav></top-nav>
    <swiper-com class="swiper"></swiper-com>
    <news-cof class="news"></news-cof>
    <!-- <router-link> -->
      <bottom-view class="bottom"></bottom-view>
    <!-- </router-link> -->

    <br>
  </div>
  <!-- <router-view/> -->
  

</template>

<script>
// @ is an alias to /src

import topNav from '@/components/topNav.vue'
import swiperCom from '@/components/swiperCom.vue'
import newsCof from '../components/newsCof.vue'
import bottomView from '../components/bottomView.vue'

export default {
  name: 'HomeView',
  components: {
    topNav,
    swiperCom,
    newsCof,
    bottomView
}
}
</script>

<style lang="less" scoped>
.home{
  text-align: center;
  background: #faf8ef;
}

.swiper{
  margin-top: 24px;
}

// .news{
//   // margin-top: 48px;
// }

.bottom{
  position: fixed;
  bottom: 0;
  width: 100%;
}

</style>