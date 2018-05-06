# Lumen | Laravel + nginx + php7.0-fpm Docker compose

An easy way to setup your lumen|laravel application using Docker and docker-compose. This will setup a developement environment with PHP7-fpm, mysql and Nginx

### Structure
~~~
├── app
│   └── public
│       └── index.php
├── nginx
│   ├── Dockerfile
|   ├── nginx.conf
│   └── app.conf
├── php-fpm
│   ├── Dockerfile
├── docker-compose.yml
├── provision
│   ├── composer_provision.sh
|   ├── git_provision.sh
|   ├── lumen_provision.sh
│   └── laravel_provision.sh
~~~
### Usage
clone this repository on your local or remote server.`docker-compose.yml` contains all your configurations you need.
you can set any laravel|lumen environment's variables in php-fpm section . database settings also is placed at db section.

your code base will puted in `/var/www/html/app`. if you need to change that you can change nginx configuration. 
finally configure your repository, and run `sudo docker-compose up`

### Additional settings 
if you need to custom nginx, or php setting you may change the appropriate files in their folders.

### Ubuntu users 
as you know nginx docker image is based on debian distrobution, so you should take care of settins.

### Contribution
please feel free to create any PR, and extending this library


