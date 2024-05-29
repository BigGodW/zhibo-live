<script setup>
import { ref } from 'vue'
const props = defineProps(['title', 'liveUrl', 'icon'])
const iframe = ref(null)
const newSrc = ref('')
// 刷新
const reload = () => {
    console.log('刷新')
    iframe.value.src = props.liveUrl
}
// 全屏
const fullPage = () => {
    console.log('全屏')
    iframe.value.requestFullscreen()
}
// 修改重置
const change = ()=>{
    console.log('重新设置地址')
}
</script>
<template>
    <div class="w-full h-screen overflow-hidden">
        <h1 class=" flex justify-center text-2xl my-1 items-center gap-3">
            <svg class="icon text-3xl" style="" aria-hidden="true">
                <use :xlink:href="'#' + icon"></use>
            </svg>
            {{ title }}
            <!-- 刷新图标 -->
            <button @click="reload">
                <svg class="icon text-3xl" aria-hidden="true">
                    <use xlink:href="#icon-shuaxin"></use>
                </svg>
            </button>
            <!-- 全屏按钮 -->
            <button class="" @click="fullPage"><svg class="icon text-3xl" style="" aria-hidden="true">
                    <use xlink:href="#icon-quanping"></use>
                </svg></button>
            <div>
                <SetLive @changeurl="(newUrl)=>{ alert(newUrl)}"></SetLive>
            </div>    
        </h1>

        <iframe class=" max-w-[450px] mx-auto w-full min-w-[300px] 
        h-full  pb-[40px]" ref="iframe" allow="fullscreen" :src="liveUrl">
        </iframe>

    </div>
</template>