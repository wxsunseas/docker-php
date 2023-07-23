FROM php:7.4.28-fpm

ENV DEBIAN_FRONTEND noninteractive

RUN  sed -i s@/archive.ubuntu.com/@/mirrors.aliyun.com/@g /etc/apt/sources.list
RUN  sed -i s@/security.debian.org/@/mirrors.aliyun.com/@g /etc/apt/sources.list 
RUN  sed -i s@/deb.debian.org/@/mirrors.aliyun.com/@g /etc/apt/sources.list 
RUN apt-get clean

RUN apt-get update && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev
# RUN apt-get install php7.0-mysql
RUN apt-get install -y \
        libicu-dev \
        libonig-dev \
        libpng-dev \
        libzip-dev \
        zip 
RUN  docker-php-ext-install \
        intl \
        mbstring \
        pdo \
        pdo_mysql \
        gd \
        zip

EXPOSE 9000