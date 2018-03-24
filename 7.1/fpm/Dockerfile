# based on Alpine 3.6
FROM alpine:3.6

# add php 7 and apache
RUN apk add --no-cache \
  php7 \
  php7-fpm \
  php7-gd \
  php7-simplexml \
  php7-redis \
  php7-mysqli \
  php7-zlib \
  php7-mbstring

EXPOSE 9000

# run
CMD ["/usr/sbin/php-fpm7", "--nodaemonize"]
