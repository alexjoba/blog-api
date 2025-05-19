# 博客

## 运行环境
- PHP 8.2
- [Laravel 11](https://learnku.com/docs/laravel/11.x)
- MySQL 8.0

## 开发配置
- [laravel-ide-helper](https://github.com/barryvdh/laravel-ide-helper)

## 接口文档

## 安装
```bash
# 安装依赖
composer install

# 复制配置文件
cp .env.example .env

# 生成JWT秘钥
php artisan jwt:secret
```

## 编码建议

- 数据库表、列名使用 `snake_case`
- 公用的服务放入 `app/Services` 目录
- Api 使用 `Response::format` 返回数据
- Api 返回单个模型时用 `XxxResource::make()`
- Api 返回多个模型时用 `XxxResource::collection()`
- Api 返回分页时用 `XxxCollection::make()`
- migration 推送到阿里云后不可再做更改（变更数据表结构）
- 业务逻辑放入`app/Logics`目录
