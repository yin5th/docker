# Based on docker image nginx
# Add some softwares or php extensions that laravel5.5(or higher) needs.
# Added softwares lists:composer

FROM nginx 
MAINTAINER yin5th "541304803@qq.com"

# Create the virtual host configuration file directory
#RUN mkdir -p /etc/nginx/sites-enabled

# Copy nginx.conf
ADD config/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80
EXPOSE 443 
