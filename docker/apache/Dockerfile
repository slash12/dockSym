FROM httpd:2.4

RUN apt update; \
    apt upgrade -y;

# install 
RUN apt-get install nano -y

WORKDIR /var/www/html/vue/
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install nodejs -y
COPY ./vue/ /var/www/html/vue/
RUN npm install

# Copy apache vhost file to proxy php requests to php-fpm container
# COPY demo.apache.conf /usr/local/apache2/conf/demo.apache.conf

# RUN echo "Include /usr/local/apache2/conf/demo.apache.conf" \
#     >> /usr/local/apache2/conf/httpd.conf