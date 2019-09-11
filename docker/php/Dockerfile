FROM php:7.3-fpm

RUN apt update; \
    apt upgrade -y

RUN apt-get install libxml2-dev -y

RUN apt-get install -y \
        libzip-dev \
        zip \
  && docker-php-ext-configure zip --with-libzip \
  && docker-php-ext-install zip

RUN docker-php-ext-install mysqli mbstring pdo pdo_mysql xml

RUN apt-get -y install curl gnupg

WORKDIR /var/www/html/symfony/
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
COPY ./symfony/ /var/www/html/symfony/
RUN composer install