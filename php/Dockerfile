FROM php:8.0-apache

RUN apt-get update && apt-get install -y libonig-dev libzip-dev git vim unzip && \
    docker-php-ext-install pdo_mysql mysqli mbstring zip && \
    a2enmod rewrite

WORKDIR /var/www/src

COPY --from=composer:2.2.5 /usr/bin/composer /usr/bin/composer