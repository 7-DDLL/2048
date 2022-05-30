<template>
  <div class="other">
    <div class="all">
        <div class="left">
            <ul class="mdui-list" v-show="index==0">
                <li class="mdui-list-item mdui-list-item-active mdui-ripple" @click="choose1">纪念奖牌</li>
                <li class="mdui-list-item mdui-ripple" @click="choose2">饰品衣物</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">支持</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">2048</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">老少皆宜</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">谁不喜欢</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">你说对吧</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">还能写点</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">什么东西</li>
                <br>
            </ul>

            <ul class="mdui-list" v-show="index==1">
                <li class="mdui-list-item mdui-ripple" @click="choose1">纪念奖牌</li>
                <li class="mdui-list-item mdui-list-item-active mdui-ripple" @click="choose2">饰品衣物</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">支持</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">2048</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">老少皆宜</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">谁不喜欢</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">你说对吧</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">还能写点</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">什么东西</li>
                <br>
            </ul>

            <ul class="mdui-list" v-show="index==2">
                <li class="mdui-list-item mdui-ripple" @click="choose1">纪念奖牌</li>
                <li class="mdui-list-item mdui-ripple" @click="choose2">饰品衣物</li>
                <li class="mdui-list-item mdui-list-item-active mdui-ripple" @click="choose3">支持</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">2048</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">老少皆宜</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">谁不喜欢</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">你说对吧</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">还能写点</li>
                <li class="mdui-list-item mdui-ripple" @click="choose3">什么东西</li>
                <br>
            </ul>
        </div>

        <div class="right">
            <div class="shoplist" v-show="index==0">
                <!-- <shop-list-item>
                </shop-list-item> -->
                <!-- <ul  v-for="(item,id) in list" :key="id">
                  <div class="single">
                    <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:0} });">
                      <img src="../assets/img/2.webp"/>
                      <div class="mdui-grid-tile-actions">
                          <div class="mdui-grid-tile-text">
                              <div class="mdui-grid-tile-title">2022年2048积分最高奖章</div>
                              <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>120硬币</div>
                          </div>
                          <div class="mdui-grid-tile-buttons">
                              <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                          </div>
                      </div>
                    </div>
                  </div>
                </ul> -->

                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:0} });">
                    <img src="../assets/img/2.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">2022年2048积分最高奖章</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>120硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>
                  
                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:1} });">
                    <img src="../assets/img/4.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">2022年2048积分前十奖章</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>120硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>

                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:2} });">
                    <img src="../assets/img/6.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">2022年2048参与奖</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>180硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>


                <div class="others">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:0} });">
                    <img src="../assets/img/2.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">其他</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>120硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>                

            </div>


            <div class="shoplist" v-show="index==1">

                <div class="single">
                  <div class="mdui-grid-tile"  @click="this.$router.push({ name: 'shopinfo',params:{id:3} });">
                    <img src="../assets/img/5.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">2048耳环</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>69硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>
                  
                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:4} });">
                    <img src="../assets/img/3.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">2048八角帽</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>69硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>

                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:5} });">
                    <img src="../assets/img/2.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">2048福袋</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>99硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>


                <div class="others">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:0} });">
                    <img src="../assets/img/2.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">其他</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>120硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>     

            </div>


            <div class="shoplist" v-show="index==2">
                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:6} });">
                    <img src="../assets/img/3.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">100积分</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>10硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>
                  
                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:7} });">
                    <img src="../assets/img/4.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">500积分</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>49硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>

                <div class="single">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:8} });">
                    <img src="../assets/img/2.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">1000积分</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>98硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>


                <div class="others">
                  <div class="mdui-grid-tile" @click="this.$router.push({ name: 'shopinfo',params:{id:0} });">
                    <img src="../assets/img/2.webp"/>
                    <div class="mdui-grid-tile-actions">
                        <div class="mdui-grid-tile-text">
                            <div class="mdui-grid-tile-title">其他</div>
                            <div class="mdui-grid-tile-subtitle"><i class="mdui-icon material-icons">grid_on</i>120硬币</div>
                        </div>
                        <div class="mdui-grid-tile-buttons">
                            <button class="mdui-btn mdui-btn-icon"><i class="mdui-icon material-icons">star_border</i></button>
                        </div>
                    </div>
                  </div>
                </div>     
                

            </div>

            <br>
            <br>


        </div>
    </div>

  </div>
</template>

<script>
import { reactive, toRefs} from 'vue'
// import shopListItem from '@/components/shopListItem.vue'
export default {
  
  components: {
      
    },
    props:{
        goods:{
            type:Array,
            default(){
                return []
            }
        }
    },
    setup(){

        const state = reactive({
            count: 0,
            index: 0,
            isshow:true,
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
        
      

        // let currentType = ref('sales')
        // const showGoods = computed(() => {
        //   return goods[currentType.value]
        // })

        // const tabclick = (index) =>{
        //   let types =['sales','new','recommend']
        //   currentType.value =types[index]
        // }

        const choose1 = () =>{
            // currentType.value = 'sales';
            state.index=0;
        }

        const choose2 = () =>{
            // currentType.value = 'new';
            state.index=1;
        }

        const choose3 = () =>{
            // currentType.value = 'recommend';
            state.index=2;
        }

        return {
            ...toRefs(state),
            
            // tabclick,
            // showGoods,
            choose1,
            choose2,
            choose3
        }
    }


}
</script>

<style scoped>
.other{
    text-align: center;
    background: #faf8ef;
    height: 900px;
    
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
    width: 36%;
    height: 700px;
}
.all{
    height: 160px;
}
.shoplist{
  width: 360px;

  padding: 8px;
  text-align: center;
}

.single{
  padding: 8px;
  margin-left: 0px;
  text-align: center;
}
.others{
  margin-left: 120px;
  padding: 8px;
}

.mudi-list-item{
  text-align: center;
}
</style>
