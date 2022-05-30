<template>
  <div class="other">
    <div class="single">
        

        <div class="right">
            <div class="mdui-grid-tile">
                <img src="list[this.$route.params.id].url"/>
                <!-- <img :src="product.url" alt=""> -->
                <div class="mdui-grid-tile-actions">
                    <div class="mdui-grid-tile-text">
                        <div class="mdui-grid-tile-title">{{list[this.$route.params.id].title}}</div>
                        <!-- <div class="mdui-grid-tile-title">{{product.title}}</div> -->
                        <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>{{list[this.$route.params.id].price}}硬币</div>
                        <!-- <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>{{product.price}}硬币</div> -->
                    </div>
                    <div class="mdui-grid-tile-buttons">
                        <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                    </div>
            </div>
        </div>

        </div>
    </div>
    

  </div>
</template>

<script>

import { reactive, toRefs } from 'vue'

export default {
  props:{
        product: Object,
        default () {
            return {}
        }
    },
    setup () {
        const state = reactive({
            count: 0,
            list: [
              {
                id: 0,
                url: require('../assets/img/2.webp'),
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
            ]
        })
    
        return {
            ...toRefs(state)
        }
    }
}
</script>

<style scoped>
.other{
    text-align: center;
    background: #faf8ef;
    
}

</style>
