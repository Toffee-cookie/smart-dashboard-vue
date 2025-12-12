<template>
  <div id="app">
    <h1>🎉 Vercel部署测试成功！</h1>
    <p>智能数据看板与分析平台</p>
    <p>部署时间: {{ new Date().toLocaleString() }}</p>
  </div>
</template>

<script setup lang="ts">
// 空的script，只是确保是Vue 3 setup语法
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
