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
        <div class="hero min-h-screen bg-base-200">
            <LiveSet></LiveSet>
            <div class="hero-content flex-col lg:flex-row-reverse hidden">
                <div>
                    <h1 class="text-2xl text-center sm:text-left sm:text-5xl font-bold">直播弹幕系统</h1>
                    <p class="py-6 sm:text-3xl pr-9">
                        多平台同步直播的优势在于能够充分利用各个平台的资源和优势，实现直播内容的最大化利用。通过在不同的平台上进行直播，可以吸引更多的观众和粉丝，增加互动和参与度，提高直播的效果和收益。
                    </p>
                    <div class="avatars my-12">
                        <div class="avatar-group -space-x-4 rtl:space-x-reverse">
                            <div class="avatar" v-for="item in lives">
                                <div class=" sm:w-24">
                                    <svg class="icon text-6xl sm:text-8xl bg-white"   aria-hidden="true">
                                        <use :xlink:href="'#icon-'+ item.icon"></use>
                                    </svg>
                                </div>
                            </div>
                            <!-- <div class="avatar">
                                <div class="w-24 bg-white">
                                    <svg class="icon text-8xl" style=""  aria-hidden="true">
                                        <use xlink:href="#icon-gengduo1"></use>
                                    </svg>
                                </div>
                            </div> -->
                        </div>
                    </div>
                   <div class=" space-x-2">
                    <button class="btn btn-primary">
                        <NuxtLink to="/live">直播后台</NuxtLink>
                    </button>
                    <button class="btn btn-info">
                        <NuxtLink to="https://www.123pan.com/s/UNqpjv-uI3GA.html">资源包下载</NuxtLink>
                    </button>
                   </div>
                </div>
            </div>
        </div>
    </div>
</template>