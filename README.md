# 苍穹外卖 (Sky Take Out)

基于 Java + Spring Boot 开发的外卖管理平台

## 项目简介

苍穹外卖是一个功能完整的外卖管理系统，包含管理端和用户端两个部分，实现了菜品管理、套餐管理、订单管理、数据统计等核心功能。

## 技术栈

- **后端框架**: Spring Boot
- **开发语言**: Java
- **数据库**: MySQL + MyBatis
- **缓存**: Redis
- **文件存储**: 阿里云 OSS
- **接口文档**: Swagger
- **其他**: 
  - Spring Cache（缓存管理）
  - Spring Task（定时任务）
  - Spring Transaction（事务管理）

## 项目结构

```
sky-take-out
├── sky-common        # 公共模块（工具类、常量等）
├── sky-pojo          # 实体类模块（DTO、VO、Entity）
└── sky-server        # 服务端模块（业务逻辑、控制器等）
```

## 核心功能

### 管理端功能
- **菜品管理**: 菜品的增删改查、分页查询、启售/停售
- **套餐管理**: 套餐的增删改查、关联菜品管理
- **分类管理**: 菜品分类和套餐分类管理
- **订单管理**: 订单查询、订单状态管理
- **数据统计**: 
  - 营业额统计
  - 订单统计
  - 用户统计
  - 菜品/套餐概览
  - 数据报表导出

### 用户端功能
- 菜品浏览
- 购物车管理
- 订单下单
- 订单查询

## 快速开始

### 前置要求

- JDK 1.8+
- Maven 3.x
- MySQL 5.7+
- Redis

### 运行步骤

1. 克隆项目
```bash
git clone https://github.com/colinill/sky-take-out.git
cd sky-take-out
```

2. 配置数据库和 Redis
   - 创建数据库
   - 修改 `application.yml` 配置文件中的数据库和 Redis 连接信息

3. 配置阿里云 OSS
   - 修改 `application.yml` 中的 OSS 相关配置

4. 启动项目
```bash
mvn clean install
cd sky-server
mvn spring-boot:run
```

5. 访问接口文档
   - 管理端接口: `http://localhost:8080/doc.html`
   - 用户端接口: `http://localhost:8080/doc.html`

## 项目特色

- ✅ 模块化设计，代码结构清晰
- ✅ 使用 Redis 缓存提升性能
- ✅ 集成 Swagger 自动生成接口文档
- ✅ 支持定时任务处理订单状态
- ✅ 完善的事务管理和异常处理
- ✅ 集成阿里云 OSS 实现图片上传
