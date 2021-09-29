# att utöka storleken.
- https://kinsta.com/se/blog/wordpress-maximala-filuppladdningsstorlek/ 
- https://kinsta.com/se/blog/wordpress-maximala-filuppladdningsstorlek/#modify-server-settings

docker
1. https://stackoverflow.com/questions/42983276/wordpress-docker-wont-increase-upload-limit 

Ändra volumens för wordpress:
```
volumes: 
       - ./uploads.ini:/usr/local/etc/php/conf.d/uploads.ini
volumes:
    db_data:
    
```

**uploads.ini**
```
file_uploads = On
memory_limit = 500M
upload_max_filesize = 500M
post_max_size = 500M
max_execution_time = 600

```

docker
```

I discovered my problem.

docker-compose kill will kill a container but rebuild it from a cache. Meaning no changes to my files were taking place.

Use docker-compose up -d --build

```
