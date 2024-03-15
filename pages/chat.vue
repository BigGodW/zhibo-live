<script setup>
const liveList = [
    {title: "微信-视频号", icon: 'icon-weixin',liveUrl:"https://channels.weixin.qq.com/platform/live/liveBuild"}, 
    { title: "抖音直播",icon:"icon-douyin",liveUrl:"https://live.douyin.com/215450079114" }, 
    { title: "快手直播",icon:"icon-kuaishou",liveUrl:"https://live.kuaishou.com/u/3xgg5x5x6f4w6em" }
]
</script>
<template>
    <div>
        <h1>客服系统</h1>
        <div class="flex justify-between overflow-auto">
            <LiveItem class=" flex-1" v-for="item in liveList" :title="item.title" :liveUrl="item.liveUrl" :icon="item.icon"></LiveItem>
        </div>
    </div>
</template>