<template>
  <view>
    <u-text text="筛选"></u-text>
    <u-grid col="2">
      <u-grid-item v-for="item in canteenList" :key="item.id">
        <canteen-item></canteen-item>
      </u-grid-item>
    </u-grid>
  </view>
</template>

<script setup lang="ts">

import CanteenItem from "@/components/canteen-item.vue";
import {ref} from "vue";

const canteenList = ref([
  {id: 1, name: '学生第一食堂'},
  {id: 2, name: '学生第二食堂'},
  {id: 3, name: '学生第三食堂'},
  {id: 4, name: '学生第四食堂'},
  {id: 5, name: '学生第五食堂'},
  {id: 6, name: '学生第六食堂'},
  {id: 7, name: '民族食堂'},
  {id: 8, name: '教工一食堂'},
  {id: 9, name: '学生第九食堂'},

]);

</script>


<style scoped lang="scss">

</style>
