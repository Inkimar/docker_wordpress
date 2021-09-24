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
