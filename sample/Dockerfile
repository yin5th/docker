FROM ubuntu:18.04
MAINTAINER yin5th "541304803@qq.com" 
ENV REFRESHED_AT 2018-06-01

RUN apt-get -qq update && apt-get -qq install nginx

RUN mkdir -p /var/www/html/website
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/

EXPOSE 80
