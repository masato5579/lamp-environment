FROM php:8.4-fpm

# カスタムPHP設定をコピー
COPY php.ini /usr/local/etc/php/

# 必要なツールとライブラリをインストール
RUN apt-get update && apt-get install -y \
    git \
    curl \
    zip \
    unzip \
    libzip-dev

# Redisをインストール
RUN git clone https://github.com/phpredis/phpredis.git /usr/src/php/ext/redis

# PHP拡張をインストール
RUN docker-php-ext-install \
    pdo_mysql \
    bcmath \
    pcntl \
    redis \
    zip

# Composerをインストール
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# ワーキングディレクトリを設定
WORKDIR /var/www/html
