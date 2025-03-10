# CRMNB商城系统

## 项目介绍
CRMNB商城系统是一套基于Laravel和Livewire开发的现代化电商系统解决方案。系统采用全栈架构，具有高性能、可扩展、易维护等特点，适用于各类电商业务场景。

## 技术栈

### 后端技术栈
- PHP 8.4+
- Laravel 12.x框架
- PostgreSQL数据库
- Redis缓存

### 管理后台技术栈
- Laravel 12.x框架
- Livewire 3.x全栈框架
- Alpine.js
- Blade模板引擎

### 前端技术栈
- Taro框架（Vue3）
- NutUI组件库
- Pinia状态管理
- Vite构建工具

## 环境要求
- PHP >= 8.4
- Composer
- Node.js >= 16
- PostgreSQL >= 14
- Redis >= 6.0

## 安装部署

### 后端API安装
1. 克隆项目
```bash
git clone https://github.com/runphp/crmnb.git
cd crmnb/backend
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

### 前端应用安装
1. 进入frontend目录
```bash
cd ../frontend
```

2. 安装依赖
```bash
pnpm install
```

3. 开发环境运行（以微信小程序为例）
```bash
pnpm run dev:weapp
```

4. 生产环境构建
```bash
pnpm run build:weapp
```

## 开发指南

### 目录结构
```
├── backend/                 # 后端服务（Laravel）
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
│   ├── resources/         # 前端资源
│   │   ├── js/           # JavaScript文件
│   │   ├── css/          # 样式文件
│   │   └── views/        # 视图文件
│   └── storage/           # 文件存储
├── frontend/              # 前端应用（Taro多端）
│   ├── src/               # 源代码
│   │   ├── api/          # API接口
│   │   ├── components/   # 公共组件
│   │   ├── pages/        # 页面文件
│   │   ├── assets/       # 静态资源
│   │   ├── store/        # 状态管理
│   │   └── utils/        # 工具函数
│   ├── config/           # Taro配置
│   └── package.json      # 项目配置文件
└── docs/                  # 项目文档
    ├── api/              # API文档
    ├── database/         # 数据库设计文档
    └── guide/            # 开发指南
```

### 开发规范
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

### 单元测试
项目使用Pest测试框架进行单元测试和功能测试。

1. 运行测试
```bash
php artisan test
```

2. 创建新测试
```bash
php artisan make:test ExampleTest
```

3. 测试目录结构
```
tests/
├── Feature/     # 功能测试
├── Unit/        # 单元测试
└── Pest.php     # Pest配置文件
```

4. 测试示例
```php
test('example test', function () {
    expect(true)->toBeTrue();
});
```

## 部署说明

### 后端部署
- 配置PHP环境（8.4+）
- 配置PostgreSQL、Redis
- 安装Composer依赖
- 配置.env环境变量
- 执行数据库迁移
- 配置Nginx

### 前端部署
- 安装Node.js环境
- 安装依赖：npm install
- 构建：npm run build
- 部署dist目录到服务器

### 小程序部署
- 安装Node.js环境
- 安装依赖：npm install
- 开发构建：npm run dev:weapp
- 生产构建：npm run build:weapp
- 使用微信开发者工具导入dist/weapp目录
- 配置小程序appid
- 上传发布

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

Copyright © 2025 CRMNB

## 技术支持

如果您在使用过程中遇到问题，请通过以下方式获取帮助：

- 官方文档：[文档地址]
- 问题反馈：[Issues]
- 技术社区：[社区地址]
- 商业支持：[联系方式]
