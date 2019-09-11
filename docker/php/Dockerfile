FROM php:7.3-fpm
RUN apt update; \
    apt upgrade -y;
RUN docker-php-ext-install mysqli mbstring pdo pdo_mysql
RUN apt-get -y install curl gnupg
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer