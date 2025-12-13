<template>
  <div class="app-header">
    <!-- 左侧：Logo和系统名称 -->
    <div class="header-left">
      <div class="logo" @click="goHome">
        <el-icon><DataLine /></el-icon>
        <span class="system-name">智能数据看板</span>
      </div>
    </div>

    <!-- 右侧：用户操作区 -->
    <div class="header-right">
      <!-- 全屏切换 -->
      <div class="header-item" @click="toggleFullscreen">
        <el-tooltip content="全屏切换">
          <el-icon><FullScreen /></el-icon>
        </el-tooltip>
      </div>

      <!-- 消息通知 -->
      <div class="header-item" @click="showNotifications">
        <el-badge :value="unreadCount" :max="99">
          <el-icon><Bell /></el-icon>
        </el-badge>
      </div>

      <!-- 用户信息 -->
      <el-dropdown @command="handleUserCommand">
        <div class="user-info">
          <el-avatar :size="32" :src="userInfo.avatar" />
          <span class="user-name">{{ userInfo.name }}</span>
          <el-icon><ArrowDown /></el-icon>
        </div>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item command="profile">
              <el-icon><User /></el-icon>个人中心
            </el-dropdown-item>
            <el-dropdown-item command="settings">
              <el-icon><Setting /></el-icon>系统设置
            </el-dropdown-item>
            <el-dropdown-item divided command="logout">
              <el-icon><SwitchButton /></el-icon>退出登录
            </el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, reactive } from 'vue'
import { useRouter } from 'vue-router'
import { ElMessage, ElMessageBox } from 'element-plus'
import {
  DataLine,
  FullScreen,
  Bell,
  User,
  Setting,
  SwitchButton,
  ArrowDown
} from '@element-plus/icons-vue'

const router = useRouter()

// 用户信息
const userInfo = reactive({
  id: 1,
  name: '管理员',
  avatar: 'https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png',
  role: '管理员'
})

// 未读消息数量
const unreadCount = ref(3)

// 点击Logo返回首页
const goHome = () => {
  router.push('/')
}

// 全屏切换
const toggleFullscreen = () => {
  if (!document.fullscreenElement) {
    document.documentElement.requestFullscreen()
  } else {
    if (document.exitFullscreen) {
      document.exitFullscreen()
    }
  }
}

// 显示通知
const showNotifications = () => {
  ElMessage.info(`您有 ${unreadCount.value} 条未读消息`)
  // 实际开发中这里应该打开通知面板
}

// 处理用户命令
const handleUserCommand = (command: string) => {
  switch (command) {
    case 'profile':
      router.push('/profile')
      break
    case 'settings':
      router.push('/settings')
      break
    case 'logout':
      handleLogout()
      break
  }
}

// 退出登录
const handleLogout = () => {
  ElMessageBox.confirm('确定要退出登录吗？', '提示', {
    confirmButtonText: '确定',
    cancelButtonText: '取消',
    type: 'warning'
  })
    .then(() => {
      // 实际开发中这里应该清除token和用户信息
      ElMessage.success('退出成功')
      router.push('/login')
    })
    .catch(() => {
      // 用户取消
    })
}
</script>

<style scoped lang="scss">
.app-header {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  color: white;

  .header-left {
    display: flex;
    align-items: center;

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
      cursor: pointer;
      user-select: none;
      transition: opacity 0.3s;

      &:hover {
        opacity: 0.8;
      }

      .el-icon {
        font-size: 24px;
      }

      .system-name {
        font-size: 18px;
        font-weight: bold;
        letter-spacing: 1px;
      }
    }
  }

  .header-right {
    display: flex;
    align-items: center;
    gap: 20px;

    .header-item {
      cursor: pointer;
      padding: 8px;
      border-radius: 4px;
      transition: background-color 0.3s;

      &:hover {
        background-color: rgba(255, 255, 255, 0.1);
      }

      .el-icon {
        font-size: 20px;
      }
    }

    .user-info {
      display: flex;
      align-items: center;
      gap: 10px;
      cursor: pointer;
      padding: 4px 8px;
      border-radius: 4px;
      transition: background-color 0.3s;

      &:hover {
        background-color: rgba(255, 255, 255, 0.1);
      }

      .user-name {
        font-size: 14px;
      }

      .el-avatar {
        border: 2px solid white;
      }
    }
  }
}

// 适配移动端
@media (max-width: 768px) {
  .app-header {
    padding: 0 10px;

    .header-left .logo .system-name {
      font-size: 16px;
    }

    .header-right {
      gap: 12px;

      .user-info .user-name {
        display: none;
      }
    }
  }
}
</style>
