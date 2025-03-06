# CRMNB商城系统

## 项目介绍
CRMNB商城系统是一套基于Laravel和Vue3开发的现代化电商系统解决方案。系统采用前后端分离架构，具有高性能、可扩展、易维护等特点，适用于各类电商业务场景。

## 技术栈

### 后端技术栈
- PHP 8.1+
- Laravel 10.x框架
- PostgreSQL数据库
- Redis缓存

### 管理后台技术栈
- Vue 3.x
- Element Plus UI框架
- TypeScript
- Vite
- Pinia状态管理
- Vue Router

## 环境要求
- PHP >= 8.1
- Composer
- Node.js >= 16
- PostgreSQL >= 14
- Redis >= 6.0

## 安装部署

### 后端API安装
1. 克隆项目
```bash
git clone https://github.com/runphp/crmnb.git
cd crmnb/api
```

2. 安装依赖
```bash
composer install
```

3. 环境配置
```bash
cp .env.example .env
# 编辑.env文件，配置数据库等信息
```

4. 初始化数据库
```bash
php artisan migrate
php artisan db:seed
```

5. 启动服务
```bash
php artisan serve
```

### 管理后台安装
1. 进入admin目录
```bash
cd ../admin
```

2. 安装依赖
```bash
pnpm install
```

3. 开发环境运行
```bash
pnpm dev
```

4. 生产环境构建
```bash
pnpm build
```

## 开发指南

### 目录结构
```
├── api                 # 后端API项目
│   ├── app            # 应用代码
│   ├── config         # 配置文件
│   ├── database       # 数据库迁移和种子
│   ├── routes         # 路由定义
│   └── tests          # 测试文件
├── admin              # 管理后台项目
│   ├── src           # 源代码
│   ├── public        # 静态资源
│   └── tests         # 测试文件
```

### 开发规范
- 遵循PSR-12编码规范
- 使用TypeScript进行开发
- 提交代码前进行代码格式化
- 编写单元测试

### 分支管理
- main: 主分支，用于生产环境
- develop: 开发分支，用于功能开发
- feature/*: 功能分支
- hotfix/*: 紧急修复分支

## 贡献指南
1. Fork 项目
2. 创建功能分支
3. 提交代码
4. 创建Pull Request

## 版权信息

Copyright © 2024 CRMNB

## 技术支持

如果您在使用过程中遇到问题，请通过以下方式获取帮助：

- 官方文档：[文档地址]
- 问题反馈：[Issues]
- 技术社区：[社区地址]
- 商业支持：[联系方式]
