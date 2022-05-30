<template>
  <div class="all">
    <div class="topCenter">
        <img src="../assets/icon/fanhui.png" href="#" style="width: 24px;height: 24px;" @click="this.$router.push('/shop');" />

        <span class="navBtn " >购物车</span>

    </div>

    <!-- <shop-car-item v-for="(item,index) in list" :key="index">
    test</shop-car-item> -->

    <ul class="mdui-list" v-for="(item,index) in car" :key="index">
        <li class="mdui-list-item mdui-ripple">
            <div class="mdui-list-item-avatar">
            <img :src="car[index].url"/>
            </div>
            <div class="mdui-list-item-content">
            <div class="mdui-list-item-title">{{car[index].title}}</div>
            <div class="mdui-list-item-text mdui-list-item-one-line">
                <span class="mdui-text-color-theme-text">{{car[index].price}}￥</span> 
                <button @click="add(index)">+</button>
                <a>{{car[index].collectcount}}件</a>
                <button @click="sub(index)">-</button>
            </div>
            </div>
        </li>
    </ul>
  </div>
</template>

<script>
import {  onBeforeMount, reactive, toRefs } from 'vue'
// import ShopCarItem from '@/components/shopCarItem.vue'
// import { useRouter} from 'vue-router'
import { useRoute } from 'vue-router'
// import axios from 'axios'

export default {
  components:{
    // ShopCarItem
    
  },
    setup () {
        const state = reactive({
            count: 0,
            id: 0,
            istrue:false,
            list: [
              {
                id: 0,
                url: require('@/assets/img/2.webp'),
                title: '2022年2048积分最高奖章',
                price: 120,
                collectcount: 58

              },
              {
                id: 1,
                url: require('@/assets/img/4.webp'),
                title: '2022年2048积分前十奖章',
                price: 120,
                collectcount: 10
              },
              {
                id: 2,
                url: require('@/assets/img/6.webp'),
                title: '2022年2048参与奖',
                price: 180,
                collectcount: 8
              },
              {
                id: 3,
                url: require('@/assets/img/5.webp'),
                title: '2048耳环',
                price: 69,
                collectcount: 24
              },
              {
                id: 4,
                url: require('@/assets/img/3.webp'),
                title: '2048八角帽',
                price: 69,
                collectcount: 34
              },
              {
                id: 5,
                url: require('@/assets/img/2.webp'),
                title: '2048福袋',
                price: 99,
                collectcount: 34
              },
              {
                id: 6,
                url: require('@/assets/img/3.webp'),
                title: '100积分',
                price: 10,
                collectcount: 34
              },
              {
                id: 7,
                url: require('@/assets/img/4.webp'),
                title: '500积分',
                price: 49,
                collectcount: 34
              },
              {
                id: 8,
                url: require('@/assets/img/2.webp'),
                title: '1000积分',
                price: 98,
                collectcount: 34
              }
            ],
            car: [
              {
                id: 0,
                url: require('../assets/img/2.webp'),
                title: '2022年2048积分最高奖章',
                price: 120,
                collectcount: 3

              },
              {
                id: 1,
                url: require('@/assets/img/4.webp'),
                title: '2022年2048积分前十奖章',
                price: 120,
                collectcount: 5
              }
            ]
        })
        
        // getContent(){
        //   this.id=this.$route.params.id;
        //   console.log(this.id)
        // }
        const route =useRoute()
        onBeforeMount(() => {
          // axios.get('/3.json').then(res => {
          //   state.list = res.data.list
          // }).catch(err => console(err))
        
          state.id=route.query.id;
          state.isTrue=route.query.isTrue;
          console.log(state.id);
          console.log(state.isTrue);
          // this.isTrue=this.$route.params.isTrue;
          var li;
          if(state.isTrue=="true"){
            console.log(state.isTrue);
            for(li of state.car){
              console.log(li.id)
              if(li.id==state.id){
                li.collectcount++;
                console.log(li.collectcount) 
                state.isTrue=false;
                break;
              }
            }
            if(state.isTrue=="true"){
              console.log(state.isTrue);
              state.car.push(state.list[state.id]);
              state.isTrue=false;
            }
          }
        })

        const add = (index) =>{
          state.car[index].collectcount++;
        }

        const sub = (index) => {
          if(state.car[index].collectcount > 0){
            state.car[index].collectcount--
          }
          else if(state.car[index].collectcount == 0){
            state.car.splice(index,1)
          }
        }
        return {
            ...toRefs(state),
            add,
            sub
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
        padding-left: 120px;
        margin-bottom: 4px;
    }
}

</style>