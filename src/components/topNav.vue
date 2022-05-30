<template>
  <div class="topNav">
    
    <div class="topCenter">
      <span class="navBtn " @click="this.$router.push('/shop');">周边</span>
      <span class="navBtn " @click="com">游戏</span>
      <span class="navBtn active" @click="this.$router.push('/');">论坛</span>
      <span class="navBtn " @click="this.$router.push('/other');">其他</span>
    </div>
    
  </div>
</template>

<script>
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
</script>


<style lang="less" scoped>
.topNav{
  // margin: 1rem;
  // width: 20rem;
  height: 40px;
  // display: flex;
  // justify-content: space-between;
  // align-items: center;
  // padding: 0 0.2rem;
  text-align: center;
  // background: rgb(229, 122, 161);
  padding-top: 8px;
  background: #b9b1aa;
  
  .topCenter{
    text-align: center;
    // width: 7rem;
    display: flex;
    justify-content: space-around;
    font-size: large;
    color: white;
    letter-spacing: 4px;
    .active{
      font-weight: 900;
    }
    .navBtn{
      margin: 5px;
    }
  }

}
</style>