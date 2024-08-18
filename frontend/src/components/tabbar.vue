<script setup lang="ts">
import { ref } from "vue";

const currentTab = ref(0);

function go(url: string) {
  uni.switchTab({
    url: "/pages/index/" + url
  });
}

</script>

<template>
  <u-tabbar :value="currentTab">
    <u-tabbar-item icon="home" text="首页" @click="go('index')"></u-tabbar-item>
    <u-tabbar-item icon="list" text="食堂" @click="go('canteen')"></u-tabbar-item>
    <u-tabbar-item icon="search" text="菜根一下"></u-tabbar-item>
    <u-tabbar-item icon="grid" text="分类"></u-tabbar-item>
    <u-tabbar-item icon="account" text="我的"></u-tabbar-item>
  </u-tabbar>
</template>

<style scoped>

</style>