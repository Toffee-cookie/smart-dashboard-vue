<template>
  <el-container class="layout">
    <!-- 顶部 -->
    <el-header class="header">
      <AppHeader />
    </el-header>

    <!-- 下半部分：左右结构 -->
    <el-container>
      <el-aside width="200px" class="aside">
        <SidebarMenu />
      </el-aside>

      <el-main class="main">
        <router-view />
      </el-main>
    </el-container>
  </el-container>
</template>

<script setup lang="ts">
import AppHeader from './AppHeader.vue'
import SidebarMenu from './SidebarMenu.vue'
</script>

<style scoped>
.layout {
  height: 100vh;
}
.header {
  background: none;
  padding: 0;
  height: 60px;
}

.aside {
  background: #f5f5f5;
  border-right: 1px solid #e4e7ed;
}

.main {
  background-color: #f5f7fa;
  padding: 20px;
}
</style>
