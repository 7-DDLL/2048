<template>
  <div class="other">
    <!-- <top-nav></top-nav> -->
    <div class="topCenter">
        <img src="../assets/icon/fanhui.png" href="#" style="width: 24px;height: 24px;" onclick="javascript :history.back(1);" />

        <span class="navBtn ">公告详情</span>

    </div>
    <!-- <swiper-com class="swiper"></swiper-com> -->
    <img src="../assets/img/bqb1.jpg" style="width: 200px;padding-top: 24px;">
    <div class="text">
      <a style="font-size:larger;font-weight: 500;text-align: center;padding-left: 60px;">杭州线下2048大比拼</a>
      <p class="ch">我们得知2048已经告别很多人的青春舞台，悲痛的我们不知从何宣泄，唯有踢烂2048办公楼里的消防警报，伴随着消防鸣笛起立默哀三分钟。</p>
      <p>Today, We have known that Xiami Music will quit the stage of history next month, we were upset but didn't know how to express, so we just kicked the fire alarms in the DoShit building and tributed silently with the fire honking for three minutes.
      </p>
      <p class="ch">2048员工们都是2048的忠实用户，就如冬战，他曾在其实并没有的超现实纪录短片《再见，2048》中大喊一句：“现在谁还玩2048阿！”来表达他个人对2048浓烈的爱意。
      </p>
      <p>Doshit employees are all loyal users of shrimp music, just like the winter warrior. He once yelled in the surreal documentary "goodbye, winter warrior": "who is still using shrimp now?" To express his strong love for shrimp music.
      </p>

      <p class="ch">我们决定在杭州为2048举办一场线下的喜宴，希望尽可能地集结杭州地区的2048玩家，让2048重出江湖。
      </p>
      <p>Vividly, online party couldn't represent our cherishing, so we decide to hold an offline,funeral for Xiami Music in Canton, we are willing to gather Xiami users as much as possible, to let Xiami rest in peace.
      </p>
    </div>
    <br>
    <br>
    <bottom-view class="bottom"></bottom-view>
  </div>
</template>

<script>
// import topNav from '@/components/topNav.vue'
// import SwiperCom from '@/components/swiperCom.vue'
import bottomView from '../components/bottomView.vue'

export default {
  name: 'OtherView',
  components: {
    // topNav,
    bottomView
    // SwiperCom
}
}
</script>

<style lang="scss" scoped>

.topCenter{
    height: 40px;
    padding-top: 16px;
    text-align: left;
    
    padding-left: 16px;
    background: #b9b1aa;
    justify-content: space-around;
    font-size: large;
    color: white;
    letter-spacing: 4px;
    .active{
      font-weight: 900;
    }
    .navBtn{
        padding-left: 100px;
        margin-bottom: 4px;
    }
}

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

.text{
  text-align: left;
  /* color: rgb(149, 114, 114); */
  color: rgb(101, 101, 101);
  /* word-spacing: 4px; */
  text-indent: 2rem;
  padding: 24px;
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
