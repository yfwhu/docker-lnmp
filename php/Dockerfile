ARG PHP_VERSION

FROM php:$PHP_VERSION-fpm-alpine

COPY config/php.ini /usr/local/etc/php

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    # php session保存位置
    && mkdir -p /usr/local/etc/php/session
    && apk add libpng-dev \
    && docker-php-ext-install pdo_mysql mysqli pcntl gd bcmath
