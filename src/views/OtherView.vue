<template>
  <div class="other">
    <top-nav></top-nav>
    
    <div class="mdui-card" >

      <!-- 卡片头部，包含头像、标题、副标题 -->
      <div class="mdui-card-header">
        <img class="mdui-card-header-avatar" src="../assets/img/bqb1.jpg"/>
        <div class="mdui-card-header-title">公告</div>
        <div class="mdui-card-header-subtitle">发布：潦草爱读书</div>
      </div>

      <!-- 卡片的媒体内容，可以包含图片、视频等媒体内容，以及标题、副标题 -->
      <div class="mdui-card-media">
        <img src="../assets/img/2.webp"/>

        <!-- 卡片中可以包含一个或多个菜单按钮 -->
        <div class="mdui-card-menu">
          <button class="mdui-btn mdui-btn-icon mdui-text-color-white">
            <!-- <i class="mdui-icon material-icons">share</i> -->
          </button>
        </div>
      </div>

      <!-- 卡片的标题和副标题 -->
      <div class="mdui-card-primary">
        <div class="mdui-card-primary-title">杭州线下2048大比拼</div>
        <div class="mdui-card-primary-subtitle">都来！</div>
      </div>

      <!-- 卡片的内容 -->
      <div class="mdui-card-content">“现在谁还玩2048阿！”</div>

      <!-- 卡片的按钮 -->
      <div class="mdui-card-actions">
        <button class="mdui-card-primary-subtitle" style="margin-left: 88px;" @click="this.$router.push('/otherinfo');">点击查收公告</button>
        <!-- <button class="mdui-btn mdui-ripple">action 2</button> -->
        <!-- <button class="mdui-btn mdui-btn-icon mdui-float-right"> -->
          <!-- <i class="mdui-icon material-icons">expand_more</i> -->
        <!-- </button> -->
      </div>

      <br>
      <br>
      <!-- <br>
      <br>
      <br>
      <br>
      <br> -->
      

    </div>


    <br>
    <br>
    <br>
    <br>
    <bottom-view class="bottom"></bottom-view>
  </div>
</template>

<script>
import topNav from '@/components/topNav.vue'
// import SwiperCom from '@/components/swiperCom.vue'
import bottomView from '../components/bottomView.vue'

export default {
  name: 'OtherView',
  components: {
    topNav,
    bottomView
    // SwiperCom
}
}
</script>

<style scoped>
.other{
    text-align: center;
    background: #faf8ef;
    
}
    .swiper{
        width: 200px;
        border: 1px solid rgb(238, 235, 235);
        
        padding: 1px;
        border-radius: 15px;
        background: white;
    }

.mdui-card{
  background: #faf8ef;
  margin: 24px;
  padding:8px;
  /* width: 300px; */
  /* height: 500px; */
  text-align: center;
  border: 1px solid #dad8d1;
}

.ch{
  letter-spacing: 2px;
}

.bottom{
  position: fixed;
  bottom: 0;
  width: 100%;
}
</style>
