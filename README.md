
# Trojan Marketplace

A full-stack USC campus web platform for students to **buy/sell second-hand goods** and **sublet housing**, with a future-ready architecture supporting **mobile expansion** and **high concurrency**.

一个有前端React + 后端Spring Boot的单一页应用，面向USC学生提供二手交易和房源转租功能，支持未来手机App拓展和高并发操作。

---

## 🏰 Project Overview / 项目概述
Trojan Marketplace is a React + Spring Boot web application that enables USC students to trade second-hand items and post sublet listings. 

Trojan Marketplace 是一个面向USC学生的网站，用于发布二手商品和房源信息，系统包含：
- 🔑 User authentication with JWT / JWT无状态认证
- 💬 Messaging and notifications / 消息通知功能
- 💳 Secure payments via Stripe/PayPal / 第三方支付集成
- 📃 Admin dashboard for moderation / 管理员后台
- ⚡ High-performance architecture / 性能性架构设计 (Redis, Kafka, Docker)

---

## ⚖️ Tech Stack / 技术栈

### Backend (Java) / 后端
- **Java 17+**, **Spring Boot** (MVC / WebFlux)
- **Spring Data JPA** + **MySQL/PostgreSQL**
- **Spring Security**, **JWT** auth
- **Redis** 缓存
- **Apache Kafka** 异步事件队列
- **Stripe / PayPal SDK** 支付集成
- **JUnit** 单元测试

### Frontend (React) / 前端
- **React + TypeScript**, SPA + React Router
- **Redux / React Context** 状态管理
- **Material-UI / Ant Design** 组件库
- **Axios / Fetch API** 连接API
- **Webpack / Vite** 打包
- 管理员页面可单独或分路由进入

---

## 🔄 System Modules / 系统模块

### 1. User Module / 用户模块
- Register/Login/Profile / 注册、登录、个人资料
- JWT/Session + Redis 认证

### 2. Second-Hand Listings / 二手商品模块
- CRUD 操作，图片上传
- 分类、搜索、评论

### 3. Sublet Listings / 房源信息模块
- 房源发布，地点、租金等
- 与二手模块共用逻辑

### 4. Messaging / 消息通信
- 站内短信系统
- 邮件通知 + 异步处理
- WebSocket / 轮询实现实时效果

### 5. Payments / 支付模块
- 订单生成，第三方支付SDK
- webhook回调更新订单状态
- 支持退款、抵押金操作

### 6. Admin Backend / 管理员后台
- 用户管理，文章下架
- 举报归档，资料统计
- RBAC权限访问

---

## 💡 Architecture / 架构总览

**Frontend:** React SPA → REST API  
**Backend:** Spring Boot 分层架构  
**Data:** MySQL/PostgreSQL + Redis  
**Async:** Kafka 异步队列  
**Security:** HTTPS + JWT + RBAC  
**APIs:** Stripe/PayPal + 邮件服务  

**数据流:**  
浏览器 → Nginx → 后端 → DB/缓存 → Kafka → 响应

---

## ✨ Scalability / 拓展性设计

- Stateless backend ✅ 并行性分布
- REST API 便于未来 React Native / Flutter
- JWT 统一认证机制
- CDN + Redis 缓存 + Kafka 异步队列

---

## 🚀 DevOps / 部署与开发工具

### Deployment / 部署
- Docker 封装后端/前端
- Docker Compose 本地开发环境
- AWS EC2/ECS/Fargate
- Nginx 负载均衡 + CDN 图片分发

### CI/CD
- GitHub Actions / Jenkins
- Postman / Swagger UI
- Prometheus + Grafana 监控
- Logback + Spring Actuator

### Development / 开发环境
- IntelliJ IDEA (后端)
- VS Code (前端)
- Slack / JIRA / GitHub Issues 协作

---

## 🌊 Status / 项目阶段
- Phase 1: 用户认证 + 基础架构
- Phase 2: 交易模块 + 消息 + 支付
- Phase 3: 后台管理 + 邮件 + 性能提升

---

## ✨ Roadmap / 未来设想
- Mobile app (React Native)
- 推荐系统、ElasticSearch
- 实时聊天 (WebSocket)

---

## 🛧 License
MIT License / 开源协议
