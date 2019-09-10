FROM httpd:2.4

COPY httpd-vhost.conf /usr/local/apache2/conf/extra/httpd-vhosts.conf

WORKDIR /var/www/html

COPY public_html/ /usr/local/apache2/htdocs/

# install dependencies
RUN composer install