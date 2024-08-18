<template>
  <!-- 首页 -->
  <view v-if="currentTab === 0">
    <home></home>
  </view>
  <!-- 食堂 -->
  <view v-if="currentTab === 1">
    <canteen></canteen>
  </view>

  <view>
    <u-tabbar :value="currentTab" @change="name => currentTab = name">
      <u-tabbar-item icon="home" text="首页" @click=""></u-tabbar-item>
      <u-tabbar-item icon="list" text="食堂" @click=""></u-tabbar-item>
      <u-tabbar-item icon="search" text="菜根一下"></u-tabbar-item>
      <u-tabbar-item icon="grid" text="分类"></u-tabbar-item>
      <u-tabbar-item icon="account" text="我的"></u-tabbar-item>
    </u-tabbar>
  </view>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Home from "@/pages/index/home.vue";
import Canteen from "@/pages/index/canteen.vue";

const currentTab = ref(0);

</script>


<style scoped lang="scss">

</style>
