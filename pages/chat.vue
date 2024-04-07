<script setup>
const liveList = [
    { title: "微信-视频号", icon: 'icon-weixin', liveUrl: "https://channels.weixin.qq.com/platform/live/liveBuild" },
    { title: "抖音直播", icon: "icon-douyin", liveUrl: "https://live.douyin.com/215450079114" },
    { title: "快手直播", icon: "icon-kuaishou", liveUrl: "https://v.kuaishou.com/tgEyoV" }
]
</script>
<template>
    <div class="flex justify-between overflow-auto py-[74px] -my-[74px] h-screen" >
        <LiveItem class=" flex-1 h-full" v-for="item in liveList" :title="item.title" :liveUrl="item.liveUrl"
            :icon="item.icon"></LiveItem>
    </div>
</template>