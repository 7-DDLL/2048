<template>
  <div class="other">
    <div class="single">
        
        <ul class="mdui-list">
        <li class="mdui-list-item mdui-ripple">
            <div class="mdui-list-item-avatar">
            <img src="list[this.$route.params.id].url"/>
            </div>
            <div class="mdui-list-item-content">
            <div class="mdui-list-item-title">{{list[this.$route.params.id].title}}</div>
            <div class="mdui-list-item-text mdui-list-item-one-line">
                <span class="mdui-text-color-theme-text">{{list[this.$route.params.id].price}}</span> 
            </div>
            </div>
        </li>
        <!-- <li class="mdui-divider-inset mdui-m-y-0"></li>
        <li class="mdui-list-item mdui-ripple">
            <div class="mdui-list-item-avatar">
            <img src="avatar2.jpg"/>
            </div>
            <div class="mdui-list-item-content">
            <div class="mdui-list-item-title">Summer BBQ</div>
            <div class="mdui-list-item-text mdui-list-item-one-line">
                <span class="mdui-text-color-theme-text">to Alex, Scott, Jennifer</span> - Wish I could ...
            </div>
            </div>
        </li>
        <li class="mdui-divider-inset mdui-m-y-0"></li>
        <li class="mdui-list-item mdui-ripple">
            <div class="mdui-list-item-avatar">
            <img src="avatar3.jpg"/>
            </div>
            <div class="mdui-list-item-content">
            <div class="mdui-list-item-title">Oui oui</div>
            <div class="mdui-list-item-text mdui-list-item-one-line">
                <span class="mdui-text-color-theme-text">Sandra Adams</span> - Do you have Paris reco ...
            </div>
            </div>
        </li> -->
        </ul>

        
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
            count: 0
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
