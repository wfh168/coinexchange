# coin-manager 后台管理系统

## 项目简介
本项目为数字货币交易所的后台管理系统，基于 Vue 2.x + Element-UI 实现，支持权限管理、用户管理、币种管理、公告管理等功能。

## 目录结构
```
coin-manager/
  ├─ src/
  │   ├─ api/         # 所有后端接口请求
  │   ├─ assets/      # 静态资源
  │   ├─ components/  # 公共组件
  │   ├─ config/      # 配置文件
  │   ├─ directive/   # 自定义指令
  │   ├─ filters/     # 过滤器
  │   ├─ icons/       # 图标
  │   ├─ lang/        # 多语言
  │   ├─ mock/        # mock 数据
  │   ├─ router/      # 路由
  │   ├─ store/       # Vuex 状态管理
  │   ├─ styles/      # 样式
  │   ├─ utils/       # 工具函数
  │   ├─ vendor/      # 第三方库
  │   └─ views/       # 业务页面
  ├─ public/          # 公共资源
  ├─ package.json     # 项目依赖
  └─ ...
```

## 安装与启动
1. 安装依赖
   ```bash
   npm install
   ```
2. 启动开发环境
   ```bash
   npm run dev
   ```
3. 打包生产环境
   ```bash
   npm run build:prod
   ```
4. 默认访问地址：http://localhost:9528

## 主要功能
- 用户/角色/权限管理
- 币种管理
- 资产管理
- 公告管理
- 统计报表
- 日志管理

## 常见问题
- 建议使用 Node.js 10 及以上版本
- 如遇依赖安装缓慢可切换为淘宝源
- 后端服务需先启动，前端接口才可正常访问

---
如有问题欢迎提 Issue 或 PR 贡献！