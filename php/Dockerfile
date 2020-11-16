FROM php:7.1-fpm

MAINTAINER Andrew Boldyrev <angelcorpc@ya.ru>

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y libmagickwand-dev --no-install-recommends
RUN pecl install -f imagick && docker-php-ext-enable imagick
RUN docker-php-ext-install mysqli pdo pdo_mysql intl
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
 	php composer-setup.php && \
 	php -r "unlink('composer-setup.php');" && \
 	mv ./composer.phar /usr/local/bin/composer

ADD ./php.ini /usr/local/etc/php/php.ini

RUN rm -rf /var/lib/apt/lists/*
RUN apt-get autoremove
RUN apt-get clean all

WORKDIR /var/www