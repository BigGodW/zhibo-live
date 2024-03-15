<script setup>
useHead({
  script: [{ src: "https://at.alicdn.com/t/c/font_4468015_5bz77qzkqio.js" }]
})

</script>
<template>
  <div>
    <nav>
      <div class="navbar bg-base-100">
        <div class="flex-1">
          <a class="btn btn-ghost text-xl" href="/">
            <svg class="icon text-5xl" aria-hidden="true">
              <use xlink:href="#icon-guanlianzhibopingtai"></use>
            </svg>
            直播弹幕系统</a>
        </div>
        <div class="flex-none">
          <ul class="menu menu-horizontal px-1">
            <li>
              <NuxtLink href="/">首页</NuxtLink>
            </li>
            <li>
              <NuxtLink href="/live">
                <svg class="icon text-2xl" aria-hidden="true">
                  <use xlink:href="#icon-daihuozhubo"></use>
                </svg>
                主播后台
              </NuxtLink>
            </li>
            <li>
              <NuxtLink href="/chat">
                <svg class="icon text-2xl" aria-hidden="true">
                  <use xlink:href="#icon-jingdiandanmu"></use>
                </svg>
                客服后台
              </NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <NuxtPage />
    <footer class="footer items-center p-4 px-12 bg-neutral text-neutral-content">
      <aside class="items-center grid-flow-col">
        <svg class="icon text-4xl" aria-hidden="true">
              <use xlink:href="#icon-guanlianzhibopingtai"></use>
            </svg>
        <p>Copyright © 2024 - All right reserved 吴八哥科技工作室</p>
        <p>蜀ICP备19039835号-2</p>
      </aside>
      <nav class="grid-flow-col gap-4 md:place-self-center md:justify-self-end">
        <!-- 电话 -->
        <a><svg class="icon text-3xl" aria-hidden="true">
              <use xlink:href="#icon-dianhua"></use>
            </svg>
        </a>
        <!-- 微信 -->
        <a>
          <svg class="icon text-3xl" aria-hidden="true">
              <use xlink:href="#icon-weixin"></use>
            </svg>
        </a>
      </nav>
    </footer>
  </div>
</template>
<style type="text/css">
.icon {
  width: 1em;
  height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>
