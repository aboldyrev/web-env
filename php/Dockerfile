FROM php:7.2-fpm
RUN apt-get update
RUN apt-get install -y libicu-dev libpng-dev
RUN docker-php-ext-install mbstring json intl gd pdo pdo_mysql mysqli