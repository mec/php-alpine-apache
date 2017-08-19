# About this Repo

This is the git repo of my Docker image for php. See the [Docker Hub Page](https://hub.docker.com/r/mecrawlings/php/) for more info.  

## Docker run
Run a detached container mapping port 80 of the container to port 80 on the host:

`$ docker run -d -p 80:80 mecrawlings/php:5.6-apache`

`$ docker run -d -p 80:80 mecrawlings/php:7.1-apache`

## Docker file

```
FROM mecrawlings/php:7.1-apache  
COPY /app/ /var/www/localhost/htdocs/
```
