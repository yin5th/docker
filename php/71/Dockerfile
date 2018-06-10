# Based on docker image php:7.1-fpm
# Added softwares lists:composer

FROM php:7.1-fpm
MAINTAINER yin5th "541304803@qq.com"

# Update package lists
RUN apt-get update

# Add composer and change the mirror source of composer to the domestic mirror
RUN curl -sS https://getcomposer.org/installer | php && \
mv composer.phar /usr/local/bin/composer && \
composer config -g repo.packagist composer https://packagist.phpcomposer.com

RUN mkdir -p /data
VOLUME ["/data"]
