<script setup>
const lives = [
    {name:"抖音",icon:"douyin"},
    {name:"快手",icon:"kuaishou"},
    {name:"微信",icon:"weixin"},
    {name:"淘宝",icon:"taobao"},
    {name:"支付宝",icon:"zhifubaozhifu"},
    {name:"其他",icon:"gengduo1"},
    ]
</script>
<template>
    <div>
        <div class="">
        <h1 class="text-3xl font-bold my-4 text-center">选择直播平台选择</h1>
        <div class="flex flex-wrap m-4 justify-center">
            <div class="flex m-2 items-center " v-for="i in lives">
                <input type="checkbox" checked="checked" class="checkbox" :id="i.icon" />
                <label class="mx-3 flex flex-col items-center" :for="i.icon">
                    <span>{{ i.name }}</span>
                    <svg class="icon text-5xl" aria-hidden="true">
                        <use :xlink:href="'#icon-'+ i.icon"></use>
                    </svg>
                </label>
            </div>
        </div>
        <img src="https://bgwblog.wubug.cn/%E7%9B%B4%E6%92%AD.png" class="max-w-[880px] mx-auto w-full px-[50px]" alt="">
    </div>
    </div>
</template>