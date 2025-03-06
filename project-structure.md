# 商城项目目录结构规划

## 目录结构

```
├── admin/                  # 管理后台（Vue3 + Element Plus）
│   ├── src/                # 源代码
│   │   ├── api/           # API接口
│   │   ├── assets/        # 静态资源
│   │   ├── components/    # 公共组件
│   │   ├── features/      # 功能模块
│   │   │   ├── system/     # 系统管理
│   │   │   ├── product/    # 商品管理
│   │   │   ├── order/      # 订单管理
│   │   │   ├── user/       # 用户管理
│   │   │   └── marketing/  # 营销管理
│   │   ├── layouts/       # 布局组件
│   │   ├── router/        # 路由配置
│   │   ├── store/         # 状态管理
│   │   ├── styles/        # 全局样式
│   │   ├── utils/         # 工具函数
│   │   └── views/         # 页面组件
│   ├── public/            # 静态公共资源
│   └── package.json       # 项目配置文件
│
├── api/                    # 后端接口服务（PHP）
│   ├── app/               # 应用目录
│   │   ├── Http/         # HTTP层
│   │   │   ├── Controllers/ # 控制器
│   │   │   ├── Middleware/ # 中间件
│   │   │   └── Requests/   # 表单请求
│   │   ├── Models/       # 数据模型
│   │   └── Services/     # 业务服务
│   ├── config/            # 配置文件
│   ├── database/          # 数据库迁移和种子
│   ├── routes/            # 路由配置
│   │   ├── api.php       # API路由
│   │   ├── admin.php     # 后台路由
│   │   └── miniapp.php   # 小程序路由
│   └── storage/           # 文件存储
│
├── miniapp/               # 小程序端（Vue3 + Taro）
│   ├── src/               # 源代码
│   │   ├── api/          # API接口
│   │   ├── components/   # 公共组件
│   │   ├── pages/        # 页面文件
│   │   ├── assets/       # 静态资源
│   │   ├── store/        # 状态管理
│   │   └── utils/        # 工具函数
│   ├── config/           # Taro配置
│   └── package.json      # 项目配置文件
│
└── docs/                  # 项目文档
    ├── api/              # API文档
    ├── database/         # 数据库设计文档
    └── guide/            # 开发指南
```

## 技术栈

### 后端（api）
- PHP 8.1+
- Laravel 10.x框架
- PostgreSQL数据库
- Redis缓存

### 管理后台（admin）
- Vue 3.x
- Element Plus UI框架
- TypeScript
- Vite
- Pinia状态管理
- Vue Router

### 小程序端（miniapp）
- Taro框架（Vue3）
- NutUI组件库
- Pinia状态管理
- Vite构建工具

## 开发规范

1. 目录命名：使用小写字母，多个单词使用连字符（-）连接
2. 文件命名：
   - 组件文件：使用PascalCase（首字母大写）
   - 其他文件：使用kebab-case（小写字母，连字符连接）
3. 代码规范：
   - 后端遵循PSR规范
   - 前端遵循ESLint + Prettier规范
4. Git分支管理：
   - main：主分支
   - develop：开发分支
   - feature/*：功能分支
   - hotfix/*：紧急修复分支

## 部署说明

1. 后端部署
   - 配置PHP环境（8.1+）
   - 配置PostgreSQL、Redis
   - 安装Composer依赖
   - 配置.env环境变量
   - 执行数据库迁移
   - 配置Nginx

2. 前端部署
   - 安装Node.js环境
   - 安装依赖：npm install
   - 构建：npm run build
   - 部署dist目录到服务器

3. 小程序部署
   - 安装Node.js环境
   - 安装依赖：npm install
   - 开发构建：npm run dev:weapp
   - 生产构建：npm run build:weapp
   - 使用微信开发者工具导入dist/weapp目录
   - 配置小程序appid
   - 上传发布