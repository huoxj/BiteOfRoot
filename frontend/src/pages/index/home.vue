<template>
  <u-notice-bar mode="closable" text="嚼个菜根小程序目前还处于测试阶段，功能尚未完善请见谅！"></u-notice-bar>
  <u-tabs :list="campusList" :scrollable="false"></u-tabs>
  <u-waterfall :model-value="menuList"  :value="menuList" add-time="50">
    <template #left="{leftList}">
      <view v-for="item in leftList" :key="item.id">
        <menu-item :menu="item" :name=item.name></menu-item>
      </view>
    </template>
    <template #right="{rightList}">
      <view v-for="item in rightList" :key="item.id">
        <menu-item :menu="item" :name=item.name></menu-item>
      </view>
    </template>
  </u-waterfall>
</template>

<script setup lang="ts">
import { ref, reactive } from 'vue'
import MenuItem from "@/components/menu-item.vue";

const campusList = reactive([
  { name: '仙林'},
  { name: '鼓楼'},
  { name: '浦口'},
  { name: '苏州'}
])

const menuList = ref([
  {id: 1, name: '川味香锅'},
  {id: 2, name: '麻辣烫'},
  {id: 3, name: '炒饭'},
  {id: 4, name: '炒面'},
  {id: 5, name: '炒河粉'},
  {id: 6, name: '炒粉丝'},
  {id: 7, name: '炒年糕'},
  {id: 8, name: '炒土豆丝'},
  {id: 9, name: '川味香锅'},
  {id: 10, name: '麻辣烫'},
  {id: 11, name: '炒饭'},
  {id: 12, name: '炒面'},
  {id: 13, name: '炒河粉'},
  {id: 14, name: '炒粉丝'},
  {id: 15, name: '炒年糕'},
  {id: 16, name: '炒土豆丝'},
])

</script>

<style>

</style>
