<script setup>
const liveList = [
    {title: "微信-视频号", icon: 'icon-weixin',liveUrl:"https://channels.weixin.qq.com/platform/live/liveBuild"}, 
    { title: "抖音直播",icon:"icon-douyin",liveUrl:"https://fxg.jinritemai.com/ffa/live_control/live/control" }, 
    { title: "快手直播",icon:"icon-kuaishou",liveUrl:"https://zs.kwaixiaodian.com/page/helper" }
]

</script>
<template>
    <div class=" w-screen">
        <div class="flex w-screen justify-center
            scale-50 sm:scale-75 md:scale-90 lg:scale-100
            
            ">
            <LiveItem class=" " v-for="item in liveList" :title="item.title" :liveUrl="item.liveUrl" :icon="item.icon"></LiveItem>
        </div>
    </div>
</template>