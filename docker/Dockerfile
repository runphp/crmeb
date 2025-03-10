FROM php:8.4-fpm

# 安装系统依赖
RUN apt-get update && apt-get install -y \
    git \
    curl \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    unzip \
    libpq-dev

# 清理apt缓存
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# 安装PHP扩展
RUN docker-php-ext-install pdo_pgsql mbstring exif pcntl bcmath gd

# 设置用户
RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

# 设置环境变量
ENV HOME=/home/www
ENV COMPOSER_HOME=/home/www/.composer
ENV PATH="/home/www/.composer/vendor/bin:${PATH}"

# 安装Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# 设置目录权限
RUN mkdir -p /home/www/.composer && chown -R www:www /home/www/.composer

# 切换到www用户
USER www

# 安装Laravel Installer
RUN composer global require laravel/installer

# 设置工作目录
WORKDIR /var/www

# 暴露端口
EXPOSE 9000