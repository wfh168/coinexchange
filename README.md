# coinexchange

## 项目简介
基于 Java 的数字货币交易所系统，支持 BTC、ETH 等主流币种，具备撮合交易引擎、账户管理、资金管理、风控、统计分析等完整功能，前后端分离，适合二次开发和学习。

## 目录结构
```
coin-exchange/         # 后端主工程（Spring Cloud 微服务架构）
  ├─ coin-admin/       # 后台管理服务
  ├─ coin-chan/        # 渠道服务
  ├─ coin-common/      # 公共模块
  ├─ coin-finance/     # 资金服务
  ├─ coin-iaas/        # 基础设施服务（网关、认证）
  ├─ coin-member/      # 用户服务
  ├─ coin-statistics/  # 统计服务
  ├─ coin-task/        # 定时任务服务
  ├─ exchange-engine/  # 交易撮合引擎
  ├─ match-engine/     # 撮合服务
  └─ pom.xml           # 后端聚合构建文件
coinexchange-ui/       # 前端工程
  ├─ coin-manager/     # 后台管理系统（基于 Vue + Element-UI）
  └─ coin-portal/      # 交易所门户（PC端，Vue）
```

## 安装与启动
### 环境要求
- JDK 1.8+
- Maven 3.5+
- Node.js 10+
- MySQL 5.7+/8.0+（需初始化数据库）

### 后端启动
1. 配置数据库、Redis、消息队列等相关环境（详见各模块 `application.yml`）。
2. 进入 `coin-exchange` 目录，执行：
   ```bash
   mvn clean install
   mvn spring-boot:run -pl coin-admin/admin-api # 启动后台API（示例）
   # 其他服务同理，或用IDEA批量启动
   ```

### 前端启动
以 coin-manager（后台管理）为例：
1. 进入 `coinexchange-ui/coin-manager` 目录
2. 安装依赖并启动开发环境：
   ```bash
   npm install
   npm run dev
   ```
3. 访问 http://localhost:9528

coin-portal（交易所门户）同理，端口和依赖见各自 package.json。

## 主要模块说明
- **coin-admin**：后台管理服务，权限、用户、币种、公告等管理
- **coin-chan**：渠道相关服务
- **coin-common**：公共依赖、工具类、常量等
- **coin-finance**：资金账户、充值、提现、流水等
- **coin-iaas**：基础设施，包含认证服务器（authorization-server）、网关（gateway-server）
- **coin-member**：会员/用户服务，注册、登录、实名认证等
- **coin-statistics**：统计分析服务
- **coin-task**：定时任务调度
- **exchange-engine**：交易撮合引擎 API/Service
- **match-engine**：撮合服务
- **coinexchange-ui/coin-manager**：后台管理前端，基于 Vue + Element-UI
- **coinexchange-ui/coin-portal**：交易所门户前端，基于 Vue

## 贡献指南
1. Fork 本仓库
2. 新建分支（如 feat_xxx）
3. 提交代码并发起 Pull Request

## 相关说明
- 各服务配置请参考对应模块的 `src/main/resources` 下的配置文件
- 前端开发建议使用 Node.js 10 及以上版本
- 如需支持多语言，可参考 Readme_zh.md、Readme_en.md

---

如有问题欢迎提 Issue 或 PR 贡献！
