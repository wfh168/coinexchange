# coin-portal 交易所门户

## 项目简介
本项目为数字货币交易所的 PC 端门户，基于 Vue 2.x + Element-UI 实现，支持行情展示、注册登录、资产管理、委托下单、K线图等功能。

## 目录结构
```
coin-portal/
  ├─ src/
  │   ├─ api/         # 所有后端接口请求
  │   ├─ assets/      # 静态资源
  │   ├─ base/        # 基础组件
  │   ├─ common/      # 公共方法/样式
  │   ├─ components/  # 公共组件
  │   ├─ plugin/      # 插件
  │   ├─ router/      # 路由
  │   ├─ store/       # Vuex 状态管理
  │   └─ ...
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
4. 默认访问地址：http://localhost:8080

## 主要功能
- 首页行情展示
- 用户注册/登录/实名认证
- 资产管理与充值提现
- 交易下单与委托管理
- K线图与深度图
- 个人中心

## 常见问题
- 建议使用 Node.js 10 及以上版本
- 如遇依赖安装缓慢可切换为淘宝源
- 后端服务需先启动，前端接口才可正常访问

---
如有问题欢迎提 Issue 或 PR 贡献！
