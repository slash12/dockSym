FROM ubuntu:latest

# install apache2
RUN apt-get update \
    && apt install apache2 -y

# Start apache2
RUN service apache2 start

# copy the vhost conf to appropriate file
# COPY httpd-vhost.conf /usr/local/apache2/conf/extra/httpd-vhosts.conf

# # install php
# RUN apt-get install php -y

# # install mysql
# RUN apt-get install mariadb-server-10.3 -y

# # install mysql
# RUN apt-get install php-mysqlnd -y

# # install php extensions
# RUN apt-get install php-apcu -y \
#     && apt-get install php-xml -y \
#     && apt-get install php7.3-zip -y

# # install curl
# RUN apt-get -y install curl gnupg

# # install git
# RUN apt-get update && \
#     apt-get upgrade -y && \
#     apt-get install -y git

# # install composer
# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# WORKDIR /usr/local/apache2/htdocs/

# # clone the project
# RUN git clone https://github.com/slash12/symRest.git

# WORKDIR /usr/local/apache2/htdocs/symRest

# # composer install
# RUN composer install