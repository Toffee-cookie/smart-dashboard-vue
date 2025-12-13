<template>
  <!-- 使用我们刚刚创建的布局组件 -->
  <BasicLayout />
</template>

<script setup lang="ts">
// 导入布局组件
import BasicLayout from '@/components/layout/BasicLayout.vue'
</script>

<style>
/* 全局样式 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  height: 100%;
  font-family:
    -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#app {
  height: 100%;
}
</style>
