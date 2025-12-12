# 📊 智能数据看板与分析平台

[![Vue 3](https://img.shields.io/badge/Vue-3.4-green)](https://vuejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue)](https://www.typescriptlang.org/)
[![Element Plus](https://img.shields.io/badge/Element_Plus-2.7-orange)](https://element-plus.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

一个基于现代化技术栈的企业级后台管理系统，专注于数据可视化与业务管理。

## ✨ 项目特点

- 🚀 **现代化技术栈**：Vue 3 + TypeScript + Vite
- 🎨 **专业UI设计**：Element Plus组件库，支持暗黑模式
- 📊 **丰富图表**：ECharts数据可视化
- 📱 **响应式设计**：适配桌面端和移动端
- 🔐 **权限管理**：基于角色的访问控制
- ⚡ **性能优化**：路由懒加载、组件异步加载
- 🛠️ **工程化规范**：ESLint + Prettier + Husky

## 📸 项目截图

> _注：项目完成后可以在这里添加截图_

<!--
![仪表盘](docs/images/dashboard.png)
![表单构建器](docs/images/form-builder.png)
![用户管理](docs/images/user-management.png)
-->

## 🏗️ 技术栈概览

### 前端框架

- **Vue 3** - 渐进式JavaScript框架
- **TypeScript** - 类型安全的JavaScript超集
- **Vite** - 下一代前端构建工具

### UI与可视化

- **Element Plus** - 企业级UI组件库
- **ECharts** - 数据可视化图表库

### 状态与路由

- **Pinia** - Vue官方推荐的状态管理
- **Vue Router 4** - 路由管理

### 开发工具

- **ESLint** - 代码质量检查
- **Prettier** - 代码格式化
- **Axios** - HTTP客户端

## 🚀 快速开始

### 环境要求

- Node.js >= 16.0.0
- npm >= 8.0.0 或 yarn >= 1.22.0

### 安装步骤

```bash
# 1. 克隆项目
git clone https://github.com/Toffee-cookie/smart-dashboard-vue.git
cd smart-dashboard-vue

# 2. 安装依赖
npm install
# 或使用 yarn
yarn install

# 3. 启动开发服务器
npm run dev
# 或
yarn dev

# 4. 打开浏览器访问
http://localhost:3000
```

其他命令：

```bash
# 代码检查
npm run lint

# 代码格式化
npm run format

# 构建生产版本
npm run build

# 预览生产构建
npm run preview

# 类型检查
npm run type-check
```

##📁 项目结构
src/
├── api/ # API接口封装
│ └── index.ts # Axios配置和请求拦截器
├── assets/ # 静态资源
│ ├── images/ # 图片资源
│ └── styles/ # 全局样式
├── components/ # 通用组件
│ ├── charts/ # 图表组件
│ ├── layout/ # 布局组件
│ └── business/ # 业务组件
├── composables/ # 组合式函数
│ └── useChart.ts # 图表相关逻辑
├── router/ # 路由配置
│ ├── index.ts # 路由定义
│ └── guards/ # 路由守卫
├── stores/ # 状态管理
│ ├── user.ts # 用户状态
│ └── app.ts # 应用状态
├── styles/ # 样式文件
│ ├── index.scss # 全局样式
│ └── variables.scss # 样式变量
├── types/ # TypeScript类型定义
│ ├── api.d.ts # API接口类型
│ └── user.d.ts # 用户相关类型
├── utils/ # 工具函数
│ ├── request.ts # 请求工具
│ └── validators.ts # 表单验证
├── views/ # 页面组件
│ ├── Dashboard/ # 数据看板
│ ├── FormBuilder/ # 表单构建器
│ ├── UserManagement/ # 用户管理
│ └── Login/ # 登录页面
├── App.vue # 根组件
└── main.ts # 应用入口

##📈 核心功能模块
###✅ 已完成
项目初始化与工程化配置

Vue 3 + TypeScript + Vite基础框架

Element Plus UI库集成

项目结构规划

Git版本控制与GitHub托管

代码规范配置(ESLint + Prettier)

###🔄 开发中
主布局组件（侧边栏+顶部导航）

路由系统与权限控制

登录认证页面

数据可视化看板

动态表单生成器

用户权限管理系统

###📅 规划中
暗黑模式切换

国际化多语言支持

主题定制系统

移动端适配优化
性能监控集成

###🛠️ 技术栈详情
核心框架
Vue 3 - 渐进式JavaScript框架

TypeScript - 类型安全的JavaScript超集

Vite - 下一代前端构建工具

UI组件库
Element Plus - 基于Vue 3的桌面端组件库

ECharts - 百度开源的可视化图表库

vue-echarts - ECharts的Vue 3组件封装

状态管理与路由
Pinia - Vue 3官方推荐的状态管理库

Vue Router 4 - Vue 3官方路由

开发工具
ESLint - 代码质量检查

Prettier - 代码格式化

Husky - Git钩子管理

Commitlint - 提交信息规范

工具库
Axios - HTTP客户端

Day.js - 轻量级日期处理库

Mock.js - 前端数据模拟

##📖 学习与开发
开发规范
组件命名: 使用PascalCase，如UserProfile.vue

文件命名: 使用kebab-case，如user-api.ts

提交信息: 遵循Conventional Commits规范

代码风格: 使用ESLint + Prettier统一代码风格

##Git工作流

```bash
# 1. 创建功能分支
git checkout -b feature/your-feature-name

# 2. 开发完成后提交
git add .
git commit -m "feat: add your feature description"

# 3. 推送到远程
git push origin feature/your-feature-name

# 4. 创建Pull Request进行代码审查
```

##🤝 贡献指南

```bash
Fork本仓库

创建功能分支 (git checkout -b feature/AmazingFeature)

提交更改 (git commit -m 'Add some AmazingFeature')

推送到分支 (git push origin feature/AmazingFeature)

开启一个Pull Request
```

##📄 许可证
本项目采用 MIT 许可证 - 查看 LICENSE 文件了解详情

##🙏 致谢
Vue.js - 渐进式JavaScript框架

Element Plus - 基于Vue 3的组件库

ECharts - 强大的图表库

Vite - 下一代前端工具

##📞 联系信息
作者: Toffee-cookie

GitHub: @Toffee-cookie

项目链接: https://github.com/Toffee-cookie/smart-dashboard-vue

<div align="center">

如果这个项目对你有帮助，请给一个 ⭐️ Star 支持！

让更多人看到这个项目，帮助更多前端开发者成长

</div> ```
