<template>
  <div class="other">
    <top-nav></top-nav>
    
    <shop-list></shop-list>

    <shop-bottom class="bottom"></shop-bottom>
  </div>
</template>

<script>
import topNav from '@/components/topNav.vue'
import shopList from '@/components/shopList.vue'
import ShopBottom from '@/components/shopBottom.vue'

export default {
  name: 'ShopView',
  components: {
    topNav,
    shopList,
    ShopBottom
}
}
</script>

<style scoped>
.other{
    text-align: center;
    background: #faf8ef;
    height: 1000px;
}
.swiper{
    width: 200px;
    border: 1px solid rgb(238, 235, 235);
    
    padding: 1px;
    border-radius: 15px;
    background: white;
}
.left{
    float: left;
}
.all{
    height: 160px;
}
.bottom{
  position: fixed;
  bottom: 0;
  width: 100%;
}
</style>
