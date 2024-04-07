<script setup>
const route = useRoute()
// 路由参数 平台: pingtia='weixin,douyin,kuaishou'
const lives = route.query.pingtai && route.query.pingtai.split(',')

const liveList = [
    {name:'weixin',title: "微信-视频号", icon: 'icon-weixin',liveUrl:"https://channels.weixin.qq.com/platform/live/liveBuild"}, 
    {name:"douyin", title: "抖音直播",icon:"icon-douyin",liveUrl:"https://fxg.jinritemai.com/ffa/live_control/live/control" }, 
    {name:"kuaishou" ,title: "快手直播",icon:"icon-kuaishou",liveUrl:"https://zs.kwaixiaodian.com/page/helper" }
]

</script>
<template>
    <div class="py-[74px] -my-[74px] h-screen">
        <div v-if="lives" class="flex w-screen justify-center
            scale-50 sm:scale-75 md:scale-90 lg:scale-100 h-full
            ">
            <div v-for="item in liveList" class="flex-1"">
                <LiveItem   :title="item.title" :liveUrl="item.liveUrl" :icon="item.icon" v-if="lives.includes(item.name) " class="flex-1"></LiveItem>
            </div>
            
        </div>
        <div v-else class="flex w-screen justify-center
            scale-50 sm:scale-75 md:scale-90 lg:scale-100 h-full
            ">
            <LiveItem  v-for="item in liveList"  :title="item.title" :liveUrl="item.liveUrl" :icon="item.icon" class="flex-1"></LiveItem>

        </div>
    </div>
</template>