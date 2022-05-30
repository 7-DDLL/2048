<template>
    <div class="all">

        <div class="topCenter">
            <img src="../assets/icon/fanhui.png" href="#" style="width: 24px;height: 24px;" onclick="javascript :history.back(1);" />

            <span class="navBtn ">商品详情</span>

        </div>


        <div class="detailList">
        
            <img :src="list[this.$route.params.id].url" alt="" style="width: 240px;">
            <h3 class="title">{{list[this.$route.params.id].title}}</h3>
            <h4 class="price">单价：<span>￥{{list[this.$route.params.id].price}}</span></h4>
            <button class="mdui-btn mdui-btn-raised mdui-ripple" @click="add(this.$route.params.id)">
            加入购物车</button>
            <!-- <el-button type="success">下单直接购买</el-button> -->
        </div>

      <shop-bottom ></shop-bottom>
      
    </div>
</template>

<script>
import { onBeforeMount, reactive, toRefs } from 'vue'
import { useRouter } from 'vue-router'
// import TopNav from '@/components/topNav.vue';
import shopBottom from '@/components/shopBottom.vue'
import axios from 'axios'
export default {
    components:{
        shopBottom
        
    },
    setup () {
        // const route =useRoute();
        const state = reactive({
            id: 1,
            list: [
             
            ]
        })

        // const route =useRouter()
        onBeforeMount(() => {
          axios.get('/3.json').then(
            res => {
            state.list = res.data.list
          }).catch(err => console(err))
        })

        // state.id=this.$route.params.type;
       const router =useRouter()
        const add = (index) =>{
            router.push({
              path: '/shopcar',
              query: { 
                id: index,
                isTrue:true }
            });
        }

        return {
            ...toRefs(state),
            add
        }
    }
}
</script>

<style lang="scss" scoped>

.all{
    background: #faf8ef;
    height: 900px;
    text-align: center;
}

.topCenter{
    height: 40px;
    padding-top: 16px;
    text-align: left;
    // width: 7rem;
    // display: flex;
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

.title,.price{
    // text-align: left;
    margin: 10px;
}
.price span{
    color: red;
}
.detailList{
    margin-top: 60px;
    height: 730px;
}
</style>