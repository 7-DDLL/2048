<template>
  <div class="bottomNav"  >
    
    <div class="mdui-bottom-nav">
  <a href="javascript:;" class="mdui-ripple mdui-bottom-nav-active">
    <!-- <i class="mdui-icon material-icons">history</i> -->
    <label></label>
  </a>
  <a href="javascript:;" class="mdui-ripple" @click="com">
    <i class="mdui-icon material-icons">favorite</i>
    <label>开始游戏</label>
  </a>

  <a href="javascript:;" class="mdui-ripple">
    <!-- <i class="mdui-icon material-icons">location_on</i> -->
    <label></label>
  </a>
</div>
    
  </div>

  
</template>


<script >
// import { onMounted } from "vue";
//引入路由
// import { useRouter } from "vue-router";

export default {
  data() {
    return {
      
    };
  },
  created() {},
  methods: {
    com() {
      window.location.href="../static/index.html"; //跳转新页面
    }
  }
};

//创建route
//  const route = useRouter();
// function com() {
// //跳转页面
//   // route.push({path:'/game'})
//   window.open("/2048", "_blank");
// }
// onMounted(() => {
  
// });

</script>


<style lang="less" scoped>
.bottomNav{
  // margin: 1rem;
  // width: 20rem;
  height: 56dp;
  // display: flex;
  // justify-content: space-between;
  // align-items: center;
  // padding: 0 0.2rem;
  text-align: center;
  // background: rgb(229, 122, 161);
  background: #b9b1aa;
  // background: rgba(238, 228, 218, 0.35);
  color: white;
  
  .topCenter{
    text-align: center;
    // width: 7rem;
    display: flex;
    justify-content: space-around;
    font-size: large;
    color: white;
    .active{
      font-weight: 900;
    }
    .navBtn{
      margin: 5px;
    }
  }

}
</style>