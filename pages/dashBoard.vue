<script setup lang='ts'>
const BaseLineChart = defineAsyncComponent(() => import('~/components/charts/BaseLineChart.vue'))
definePageMeta({
  title: '欢迎登录',
})
</script>

<template>
  <div h-full w-full overflow-hidden>
    <ClientOnly>
      <homePageDrawer />
      <a-layout h-full bg-base>
        <a-layout-content bg-base py-3 pl-8>
          <div h-full w-full flex flex-col justify-between rounded-3xl bg-main p-4>
            <div h="28.5%" w-full flex flex-col rounded-3xl bg-base>
              <div title-main>
                体重-热量变化趋势
              </div>
              <BaseLineChart flex-1 />
            </div>
            <div h="48.5%">
              <rowTwo />
            </div>
            <div h="18.5%">
              <base-scatter-diagram />
            </div>
          </div>
        </a-layout-content>
        <sideBar />
      </a-layout>
    </ClientOnly>
  </div>
</template>
