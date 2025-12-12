# 📊 智能数据看板与分析平台

[![Vue 3](https://img.shields.io/badge/Vue-3.4-green)](https://vuejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue)](https://www.typescriptlang.org/)
[![Element Plus](https://img.shields.io/badge/Element_Plus-2.7-orange)](https://element-plus.org/)
[![Vite](https://img.shields.io/badge/Vite-5.0-purple)](https://vitejs.dev/)

一个基于现代化技术栈的企业级后台管理系统，专注于数据可视化与业务管理。

## ✨ 项目特点

- 🚀 **现代化技术栈**：Vue 3 + TypeScript + Vite
- 🎨 **专业UI设计**：Element Plus组件库
- 📊 **丰富图表**：ECharts数据可视化
- 📱 **响应式设计**：适配桌面端和移动端
- 🔐 **权限管理**：基于角色的访问控制
- ⚡ **性能优化**：路由懒加载、组件异步加载
- 🛠️ **工程化规范**：ESLint + Prettier + Git钩子

## 🏗️ 技术栈

### 核心框架

- **Vue 3** - 使用Composition API构建现代化应用
- **TypeScript** - 类型安全的JavaScript超集
- **Vite** - 快速构建工具和开发服务器

### UI与可视化

- **Element Plus** - 基于Vue 3的企业级UI组件库
- **ECharts** - 数据可视化图表库，支持多种图表类型

### 状态管理与路由

- **Pinia** - Vue官方推荐的状态管理方案
- **Vue Router 4** - 路由管理，支持动态路由和权限控制

### 开发工具

- **ESLint + Prettier** - 代码质量检查和格式化
- **Axios** - HTTP客户端，处理API请求
- **Mock.js** - 前端数据模拟，便于开发和测试

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

# 3. 启动开发服务器
npm run dev

# 4. 打开浏览器访问
# http://localhost:3000
```

### 其他命令

```bash
# 代码检查
npm run lint

# 代码格式化
npm run format

# 构建生产版本
npm run build

# 预览生产构建
npm run preview
```

## 📁 项目结构

```
src/
├── api/           # API接口封装
├── assets/        # 静态资源
├── components/    # 通用组件
│   ├── charts/   # 图表组件
│   ├── layout/   # 布局组件
│   └── business/ # 业务组件
├── composables/   # 组合式函数
├── router/        # 路由配置
├── stores/        # 状态管理
├── styles/        # 样式文件
├── types/         # TypeScript类型定义
├── utils/         # 工具函数
├── views/         # 页面组件
│   ├── Dashboard/     # 数据看板
│   ├── FormBuilder/   # 表单构建器
│   ├── UserManagement/ # 用户管理
│   └── Login/         # 登录页面
├── App.vue         # 根组件
└── main.ts         # 应用入口
```

## 📈 功能规划

### ✅ 已完成

- [x] 项目初始化与工程化配置
- [x] Vue 3 + TypeScript + Vite基础框架
- [x] Element Plus UI库集成
- [x] 项目结构规划
- [x] Git版本控制与GitHub托管
- [x] 代码规范配置(ESLint + Prettier)

### 🔄 开发中

- [ ] 主布局组件（侧边栏+顶部导航）
- [ ] 路由系统与权限控制
- [ ] 登录认证页面
- [ ] 数据可视化看板
- [ ] 动态表单生成器
- [ ] 用户权限管理系统

### 📅 规划中

- [ ] 暗黑模式切换
- [ ] 国际化多语言支持
- [ ] 主题定制系统
- [ ] 移动端适配优化

## 📖 开发规范

### 组件命名

- 使用PascalCase，如 `UserProfile.vue`
- 组件目录使用kebab-case，如 `user-management/`

### 代码提交

- 遵循Conventional Commits规范
- 示例：
  - `feat: 添加用户登录功能`
  - `fix: 修复表单验证问题`
  - `docs: 更新README文档`

### Git工作流

```bash
# 创建功能分支
git checkout -b feature/your-feature

# 提交更改
git add .
git commit -m "feat: 添加新功能"

# 推送到远程
git push origin feature/your-feature
```

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 🤝 贡献指南

1. Fork 本仓库
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

## 📞 联系信息

- **作者**: Toffee-cookie
- **GitHub**: [@Toffee-cookie](https://github.com/Toffee-cookie)
- **项目链接**: [https://github.com/Toffee-cookie/smart-dashboard-vue](https://github.com/Toffee-cookie/smart-dashboard-vue)

---

<div align="center">
  
**如果这个项目对你有帮助，请给一个 ⭐️ Star 支持！**

</div>

## 🙏 致谢

感谢以下开源项目：

- [Vue.js](https://vuejs.org/)
- [Element Plus](https://element-plus.org/)
- [ECharts](https://echarts.apache.org/)
- [Vite](https://vitejs.dev/)

---

这个README格式简洁清晰，在GitHub上显示效果良好。它包含了项目的基本信息、技术栈、使用指南和开发规划，适合用于学习和展示。你可以直接复制到你的项目中。
