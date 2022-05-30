<template>
<div id="swipercom">
    <div class="swiper-container" id="swiperIndex">
      <div class="swiper-wrapper">
          <img class="swiper-slide" v-for="(item,i) in imgData" :key="i" :src="item" v-show="cur===i" />
            <!-- <img :src="item.pic" > -->
          
          
      </div>
      
  </div>
</div>
</template>

<script>

import {  provide, reactive, toRefs, onMounted } from 'vue'

export default {

    setup(){
        const state = reactive({
            imgData: [
                require('@/assets/img/6.webp'),
                require('@/assets/img/5.webp'),
                require('@/assets/img/4.webp')
            ],
            cur: 0,// 初始化值
            timer: null
        })
        provide('imgData', state.imgData)
        const autoplay = () => {
            state.cur++
            state.cur = state.cur % state.imgData.length
            // console.log(state.cur)
        }
        const play = () => {
            state.timer = setInterval(autoplay, 1000)
        }
        const stop = () => {
            clearInterval(state.timer)
        }
        const move = () => {
            play()
        }
        onMounted(() => {
            play()
        })
        
    
        return {
            ...toRefs(state),
            play,
            stop,
            move
        }
        
    }
    
}
</script>

<style lang="less" scoped>

.swiper-slide{
    width: 100%;
    // margin-top: 24px;
}

</style>