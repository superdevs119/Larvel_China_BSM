# Laravel 中国版

[![Build Status](https://travis-ci.org/zxz054321/laravel4china.svg?branch=master)](https://travis-ci.org/zxz054321/laravel4china)

对官方源码作了适量修改，使之更符合国情、更适合作为新项目基石，但不建议初学者使用。

主要特性：

1. 基于 Laravel 5.3 （版本选择的原则是：最新的稳定）
2. Laravel 安装器可一键安装框架依赖、一键执行优化、自动设置符号链接以及自动设置权限
3. Node 模块安装器可一键安装 Laravel Elixir 并执行 gulp 任务
4. 自动生成 APP_KEY
5. 内置中文语言包
6. 时区默认为中国上海
7. 更优秀的 IDE 代码提示
8. .gitignore 忽略 IDE 相关文件
9. 演示页面去除 Google 字体引用
10. 推崇 Repository 设计模式

## Laravel 安装器

此安装器脚本针对 Ubuntu 系统编写，可自动完成以下操作：

1. 全局安装 PHP Composer
2. 复制 `.env` 文件
3. 执行 `composer install --no-dev` 安装依赖
4. 执行 `php artisan key:generate` 生成App key
5. 执行优化
6. 创建符号链接（将` public/storage` 目录链接去 `storage/app/public`目录）
7. 设置应用目录用户为 `www`
8. 赋予 `bootstrap/cache` 目录和 `storage` 目录读写权限

### 使用方法

在应用根目录下执行命令：

```
sudo chmod 777 install.sh && ./install.sh
```

### 参数说明

| 参数   | 说明                                       |
| ---- | ---------------------------------------- |
| -q   | 安静模式，脚本将静默执行，适用于自动部署的场景                  |
| -e   | （安静模式下必填）指定 env 文件。示例： `-e .env.example` |
| -k   | （可选）执行 `php artisan key:generate`        |
| -o   | （可选）执行 autoload、路由、配置优化                  |

## Node 模块安装器

此安装器脚本针对 Ubuntu 系统编写，可自动完成以下操作：

1. 全局安装 Node.js v4.x LTS
2. 设置 npm 使用淘宝镜像，大大提高下载速度
3. 全局安装 gulp
4. 安装 Laravel Elixir
5. 执行 `gulp --production` 编译前端资源

### 使用方法

在应用根目录下执行命令：

```
sudo chmod 777 install-node.sh && ./install-node.sh
```

<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, yet powerful, providing tools needed for large, robust applications. A superb combination of simplicity, elegance, and innovation give you tools you need to build any application with which you are tasked.

## Learning Laravel

Laravel has the most extensive and thorough documentation and video tutorial library of any modern web application framework. The [Laravel documentation](https://laravel.com/docs) is thorough, complete, and makes it a breeze to get started learning the framework.

If you're not in the mood to read, [Laracasts](https://laracasts.com) contains over 900 video tutorials on a range of topics including Laravel, modern PHP, unit testing, JavaScript, and more. Boost the skill level of yourself and your entire team by digging into our comprehensive video library.

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](http://laravel.com/docs/contributions).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell at taylor@laravel.com. All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
