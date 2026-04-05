# 🍽️ 苍穹外卖 - Sky Take Out

<div align="center">

![Java](https://img.shields.io/badge/Java-1.8-orange?style=flat-square&logo=java)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.7.3-brightgreen?style=flat-square&logo=springboot)
![MyBatis](https://img.shields.io/badge/MyBatis-2.2.0-red?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

**一款现代化的外卖点餐系统 | A Modern Food Ordering System**

[功能特性](#-功能特性) • [技术架构](#-技术架构) • [项目结构](#-项目结构) • [快速开始](#-快速开始)

</div>

---

## 📖 项目简介

**苍穹外卖** 是一款基于 Spring Boot + MyBatis 的企业级外卖点餐系统，采用前后端分离架构，支持 **管理端** 和 **用户端** 双端应用。项目涵盖完整的餐饮业务流程，从店铺管理、菜品维护到订单处理、在线支付，一站式解决外卖平台核心需求。

> 💡 适合作为 Java Web 开发学习、毕业设计或企业级项目实践参考。

---

## ✨ 功能特性

### 🔐 管理端
| 模块 | 功能 |
|------|------|
| 👤 **员工管理** | 员工增删改查、权限控制、账号启用/禁用 |
| 📦 **分类管理** | 菜品分类、套餐分类的层级维护 |
| 🍜 **菜品管理** | 菜品信息、口味、图片、起售/停售状态 |
| 🥡 **套餐管理** | 套餐组合、套餐菜品关联、价格设置 |
| 🏪 **店铺管理** | 营业状态设置、店铺信息维护 |

### 🛒 用户端
| 模块 | 功能 |
|------|------|
| 🔑 **用户认证** | 微信登录、JWT Token 鉴权 |
| 📍 **地址管理** | 收货地址增删改查、默认地址设置 |
| 🛍️ **商品浏览** | 分类筛选、菜品详情、套餐展示 |
| 🛒 **购物车** | 加入购物车、数量调整、清空操作 |
| 📝 **订单流程** | 下单、支付（微信支付）、订单查询、历史记录 |

---

## 🏗️ 技术架构

### 后端技术栈
| 技术 | 版本 | 说明 |
|------|------|------|
| **Spring Boot** | 2.7.3 | 核心框架 |
| **MyBatis** | 2.2.0 | 持久层框架 |
| **MySQL** | - | 关系型数据库 |
| **Redis** | - | 缓存中间件 |
| **Spring Cache** | - | 缓存注解 |
| **Aliyun OSS** | 3.10.2 | 对象存储（图片托管） |
| **WeChat Pay** | 0.4.8 | 微信支付 API v3 |
| **JWT** | 0.9.1 | Token 认证 |
| **Knife4j** | 3.0.2 | API 文档增强 |
| **POI** | 3.16 | Excel 导入导出 |
| **Lombok** | 1.18.20 | 代码简化 |

### 项目架构
```
sky-take-out
├── sky-common    # 公共模块（工具类、常量、异常处理）
├── sky-pojo      # 实体模块（DTO、VO、Entity）
└── sky-server    # 服务模块（Controller、Service、Mapper）
```

---

## 🚀 快速开始

### 环境要求
- JDK 1.8+
- Maven 3.6+
- MySQL 5.7+
- Redis 6.0+

### 启动步骤

```bash
# 1. 克隆项目
git clone https://github.com/TianYou0714/sky-take-out.git

# 2. 导入数据库脚本
mysql -u root -p < sql/sky_take_out.sql

# 3. 修改配置文件
# 编辑 sky-server/src/main/resources/application-dev.yml
# 配置数据库连接、Redis、阿里云OSS、微信支付等参数

# 4. 编译打包
mvn clean package -DskipTests

# 5. 启动服务
java -jar sky-server/target/sky-server-1.0-SNAPSHOT.jar
```

### 访问地址
- 🔗 API 文档：`http://localhost:8080/doc.html`
- 🔗 管理端接口：`/admin/**`
- 🔗 用户端接口：`/user/**`

---

## 📂 项目结构

```
com.sky
├── annotation      # 自定义注解
├── aspect          # AOP 切面（日志、事务）
├── config          # 配置类（Redis、Web、Swagger）
├── controller
│   ├── admin       # 管理端接口
│   └── user        # 用户端接口
├── handler         # 全局异常处理
├── interceptor     # 拦截器（JWT 验证）
├── mapper          # MyBatis Mapper 接口
└── service         # 业务逻辑层
```

---

## 📌 核心亮点

- ✅ **前后端分离**：接口设计规范，支持多端接入
- ✅ **JWT 无状态认证**：安全可靠，易于扩展
- ✅ **Redis 缓存优化**：提升数据查询性能
- ✅ **微信生态集成**：微信登录 + 微信支付
- ✅ **AOP 切面编程**：统一日志、事务管理
- ✅ **Swagger 文档**：Knife4j 增强版，接口调试更便捷

---

<div align="center">

**⭐ 如果这个项目对你有帮助，欢迎 Star 支持！**

Made with ❤️ by [TianYou0714](https://github.com/TianYou0714)

</div>
