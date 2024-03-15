<script setup>
import {ref} from 'vue'
const props = defineProps(['title', 'liveUrl', 'icon'])
const iframe = ref(null)
const reload = ()=>{
    console.log('刷新')
    iframe.value.src = props.liveUrl
}
const fullPage = ()=>{
    console.log('全屏')
    iframe.value.requestFullscreen()
}
</script>
<template>
    <div class="border">
        <h1 class=" flex justify-center text-2xl my-1 items-center gap-3">
            <svg class="icon text-3xl" style="" aria-hidden="true">
                <use :xlink:href="'#'+ icon"></use>
            </svg>
            {{ title }}
            <!-- 刷新图标 -->
            <button class="" @click="reload">
                <svg class="icon text-3xl" style="" aria-hidden="true">
                <use xlink:href="#icon-shuaxin"></use>
            </svg>
            </button>
            <!-- 全屏按钮 -->
            <button class="" @click="fullPage"><svg class="icon text-3xl" style="" aria-hidden="true">
                <use xlink:href="#icon-quanping"></use>
            </svg></button>
        </h1>
        <div class="flex justify-center">
           
                    <div class="artboard phone-3">
                        <!-- 嵌入其他网页 -->
                        <iframe ref="iframe" scrolling="no" allow="fullscreen" :src="liveUrl" width="100%" height="100%" frameborder="0"></iframe>
                    </div>
               
        </div>
        
    </div>
</template>