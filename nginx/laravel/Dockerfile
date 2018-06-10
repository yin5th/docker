# Based on docker image nginx
FROM nginx 
MAINTAINER yin5th "541304803@qq.com"

# Apply Nginx configuration
ADD config/nginx.conf /etc/nginx/nginx.conf
RUN rm /etc/nginx/conf.d/default.conf
RUN mkdir -p /data
VOLUME ["/data"]

EXPOSE 80
EXPOSE 443 
