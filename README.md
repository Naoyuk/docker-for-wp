# docker-for-wp

## Setup
1. Move to your project directory
```
$ cd /your/project/path
```
2. Clone this repository
```
$ git clone git@github.com:Naoyuk/docker-for-wp.git
```
3. Create wordpress directory
```
$ mkdir wordpress
```
4. Put your wordpress codes to `wordpress` dir
5. Copy the wp-config-sample.php to wp-config.php.(`DB_HOST` sets 'mysql')
6. Build the docker image and up
```
$ docker-compose build
$ docker-compose up -d
```
7. Access to 'http://localhost:8080/' on your browser.
  
- If you want to use phpmyadmin, access to 'http://localhost:8000/' on your browser.
- If you want to track the server log, input the following command.
```
$ docker logs -f <php CONTAINER ID>
```

## MySQL Dump
```
$ docker exec -it <mysql CONTAINER ID> sh -c "mysqldump -u root --password=password wpdb 2> /dev/null" > mysql/db_dump/backup.sql
```
