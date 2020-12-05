ARG PHP_VERSION
FROM php:$PHP_VERSION-fpm-alpine

### set timezome
ENV TZ=Asia/Shanghai

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    # php session保存位置
    && mkdir -p /usr/local/etc/php/session \
    # 这里的php-fpm基础镜像不需要 apk update
    && apk add libpng-dev \
    && docker-php-ext-install pdo_mysql mysqli pcntl gd bcmath \
    && apk add tzdata \
    && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone
