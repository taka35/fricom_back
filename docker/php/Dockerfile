FROM php:7.4-fpm

#composerのインストール
COPY --from=composer /usr/bin/composer /usr/bin/composer

#パッケージ管理ツールapt-getの更新と必要パッケージのインストール
RUN apt-get update \
  && apt-get install -y \
  git \
  zip \
  unzip \
  && docker-php-ext-install pdo_mysql bcmath

WORKDIR /app
