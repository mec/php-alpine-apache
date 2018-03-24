# based on Alpine 3.6
FROM alpine:3.6

# add php 7 and apache
RUN apk add --no-cache \
  apache2 \
  php7-apache2 \
  php7-gd \
  php7-simplexml \
  php7-redis \
  php7-mysqli \
  php7-zlib \
  php7-mbstring \
  php7-json

# copy over some basic config
COPY localhost.conf /etc/apache2/conf.d/localhost.conf

# copy over a php info file
COPY index.php /var/www/localhost/htdocs/index.php

# make the run directory
RUN mkdir -p /run/apache2/

# route logs to stdout and stderr
RUN ln -sf /dev/stdout /var/log/apache2/access.log && \
    ln -sf /dev/stderr /var/log/apache2/error.log

# run apache in foreground
CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
