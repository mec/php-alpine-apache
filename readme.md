# About this Repo

This is the git repo of my Docker image for php.

## Docker run

``$ docker run -d -p 80:80 mecrawlings/php:5.6-apache``

``$ docker run -d -p 80:80 mecrawlings/php:7.1-apache``

## Docker file

``
FROM mecrawlings/php:7.1-apache
COPY app/ /var/www/localhost/htdocs/
``
