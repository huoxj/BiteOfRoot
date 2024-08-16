<script setup lang="ts">
import {ref} from "vue";

const props = defineProps(['name'])
const url = ref("https://cdn.uviewui.com/uview/album/".concat(Math.floor(Math.random() * 10 + 1).toString()).concat(".jpg"))


</script>

<template>
  <u-card
    :border="false"
    :head-border-bottom="false"
    padding="0"
    margin="10rpx 5rpx 5rpx 5rpx">
    <template #body>
      <image
        :src=url
        class="image"
        mode="widthFix" :lazy-load="true">
      </image>
      <u-text
        class="title"
        :text="name"
        :bold="true"
        size="33rpx"
        margin="0rpx 0rpx 10rpx 20rpx"
        wordWrap="anywhere"
        style="width: 95%"></u-text>
    </template>
  </u-card>
</template>

<style scoped>
.image{
  width: 100%;
}
</style>