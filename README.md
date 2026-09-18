# 🎓 校园二手书交易平台

> 基于 Spring Boot 3 + Vue3 重构的高校二手书交易平台 · 前后端分离 · Docker 一键部署

[![GitHub](https://img.shields.io/badge/GitHub-cenzhishan-0C447C?style=flat-square&logo=github)](https://github.com/cenzhishan/campus-bookstore)

## 📌 项目简介

本项目是广西警察学院《信息系统开发实践》课程作业的工程化升级版。

原项目仅使用 HTML / CSS / 原生 JavaScript 实现，数据存储在浏览器本地。重构版采用 **Spring Boot 3 + MyBatis-Plus + MySQL + Redis** 构建后端，**Vue3 + Element Plus + Axios** 构建前端，并通过 **Docker Compose** 实现一键部署上线。

项目目标是为高校学生提供一个安全、便捷、可信的二手书交易环境，覆盖书籍发布、搜索筛选、收藏、订单流转等完整流程。

## 🌐 在线演示

- 演示地址：http://your-demo.com/（**第 11 周部署后替换为真实公网地址**）
- GitHub 仓库：https://github.com/cenzhishan/campus-bookstore

## 🛠 技术栈

### 后端
- **Spring Boot 3** — 企业级 Java 后端框架
- **MyBatis-Plus** — 高效 ORM，简化 CRUD 与分页
- **MySQL 8** — 数据持久化
- **Redis** — 热门书目缓存、会话管理
- **JWT** — 用户登录鉴权
- **Swagger / Knife4j** — 自动生成接口文档

### 前端
- **Vue 3** — 组合式 API
- **Element Plus** — UI 组件库
- **Vue Router** — 路由管理
- **Axios** — HTTP 请求
- **Vite** — 构建工具

### 工程化与部署
- **Git** — 版本控制
- **Maven** — 后端构建
- **Docker** — 容器化部署
- **Docker Compose** — 一键启动全栈服务
- **Nginx** — 反向代理与前端托管

## ✨ 核心功能

### 用户系统
- [x] JWT 登录 / 注册 / 登出
- [x] 普通用户 / 管理员两种角色

### 书籍管理
- [x] 发布二手书（书名、分类、价格、成色、描述、图片）
- [x] 按分类、关键词、价格区间筛选
- [x] 价格升序 / 降序排序
- [x] 收藏 / 取消收藏
- [x] 书籍上下架

### 订单流程
- [x] 买家下单
- [x] 卖家确认
- [x] 订单状态流转：待付款 → 已付款 → 已发货 → 已完成

### 性能优化
- [x] Redis 缓存热门书目列表（TTL 5 分钟）
- [x] MySQL 索引优化，提升查询速度

## 📸 项目截图

> 以下截图将在第 11 周部署上线后补充

| 首页 | 书籍详情 | 后台管理 |
|---|---|---|
| ![首页](docs/screenshots/home.png) | ![详情](docs/screenshots/detail.png) | ![后台](docs/screenshots/admin.png) |

## 🚀 快速启动（本地开发）

### 1. 环境要求

- JDK 17+
- Node.js 18+
- MySQL 8+
- Redis 7+
- Maven 3.9+

### 2. 克隆仓库

```bash
git clone https://github.com/cenzhishan/campus-bookstore.git
cd campus-bookstore
```

### 3. 启动后端

```bash
cd bookstore-server
# 修改 application.yml 中的数据库配置
mvn clean install
mvn spring-boot:run
```

后端默认运行在 http://localhost:8080

### 4. 启动前端

```bash
cd bookstore-web
npm install
npm run dev
```

前端默认运行在 http://localhost:5173

### 5. 打开浏览器

访问 http://localhost:5173 即可体验。

## 🐳 Docker 一键部署

```bash
cd docker
# 修改 .env 文件中的数据库密码与端口
docker-compose up -d
```

部署完成后，访问 http://your-server-ip 即可使用。

## 📁 项目结构

```text
campus-bookstore/
├── bookstore-server/          # 后端工程
│   ├── src/main/java/         # Java 源码
│   ├── src/main/resources/    # 配置文件
│   └── pom.xml                # Maven 依赖
├── bookstore-web/             # 前端工程
│   ├── src/                   # Vue3 源码
│   ├── public/                # 静态资源
│   └── package.json           # NPM 依赖
├── docker/                    # Docker 部署脚本
│   ├── docker-compose.yml
│   ├── nginx.conf
│   └── .env.example
└── README.md
```

## 📅 开发时间线

| 时间 | 里程碑 |
|---|---|
| 2026.09.21 | 项目启动，完成 JDK / IDEA / Git 环境搭建 |
| 2026.10 | 完成 Spring Boot 后端基础架构（JWT + MyBatis-Plus + MySQL） |
| 2026.11 | 完成 Vue3 前端联调，接入后端接口 |
| 2026.11.28 | 部署到云服务器，公网可访问 |
| 2026.12 | 简历投递，持续维护与优化 |

## 🤝 后续计划

- [ ] 接入短信验证码，提升账号安全性
- [ ] 引入 Elasticsearch，增强书籍全文搜索
- [ ] 增加交易评价与信用分体系
- [ ] 接入微信小程序端

## 📧 联系我

- GitHub：[@cenzhishan](https://github.com/cenzhishan)
- 邮箱：2981519637@qq.com
- 求职意向：Java 后端 / 全栈开发实习（南宁 / 深圳）

---

> 本项目为个人学习与求职作品，代码遵循 MIT 协议开放。欢迎 Star 和 Fork。

