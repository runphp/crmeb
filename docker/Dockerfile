FROM php:8.1-fpm

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

# 安装Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# 设置工作目录
WORKDIR /var/www

# 设置用户
RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

# 设置工作目录
WORKDIR /var/www

# 切换到www用户
USER www

# 暴露端口
EXPOSE 9000