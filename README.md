# docker_wordpress
Docker Wordpress, port 8080

## dockerhub
https://hub.docker.com/_/wordpress

### original Dockerfile
https://github.com/docker-library/wordpress/blob/9954966feffdaf39082609816f896c2e3f75f0db/latest/php7.4/apache/Dockerfile 

### Adding additional libraries / extensions

This image does not provide any additional PHP extensions or other libraries, even if they are required by popular plugins (e.g. it cannot send e-mails). There are an infinite number of possible plugins, and they potentially require any extension PHP supports. Including every PHP extension that exists would dramatically increase the image size.

If you need additional PHP extensions, you'll need to **create your own image FROM this one**. 
The documentation of the php image explains how to compile additional extensions. 
Additionally, the wordpress Dockerfile has an example of doing this.

### php
https://github.com/docker-library/docs/blob/master/php/README.md#how-to-install-more-php-extensions

```
If you need additional PHP extensions, you'll need to create your own image FROM this one. 
The documentation of the php image explains how to compile additional extensions. 
Additionally, the wordpress Dockerfile has an example of doing this.
```
 see here -> https://github.com/docker-library/wordpress/blob/618490d4bdff6c5774b84b717979bfe3d6ba8ad1/apache/Dockerfile#L5-L9 

Dockerfile

```
FROM php:5.6-apache

RUN a2enmod rewrite

# install the PHP extensions we need
RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev && rm -rf /var/lib/apt/lists/* \
	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
	&& docker-php-ext-install gd
RUN docker-php-ext-install mysqli
```

