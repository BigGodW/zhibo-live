<template>
    <nav>
      <div class="navbar bg-base-100">
        <div class="flex-1">
          <a class="btn btn-ghost text-xl" href="/">
            <svg class="icon text-5xl" aria-hidden="true">
              <use xlink:href="#icon-guanlianzhibopingtai"></use>
            </svg>
            <span class="hidden sm:block">直播弹幕系统</span></a>
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
</template>