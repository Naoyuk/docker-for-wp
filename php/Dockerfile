FROM php:7.4-apache
COPY ./php.ini /usr/local/etc/php
COPY ./apache2.conf /etc/apache2/conf-enabled
RUN apt-get update \
  && apt-get install -y libonig-dev vim \
  && docker-php-ext-install mysqli pdo_mysql
