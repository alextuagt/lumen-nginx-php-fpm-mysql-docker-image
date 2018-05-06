# Lumen | Laravel + nginx + php7.0-fpm Docker compose

An easy way to setup your lumen|laravel application using Docker and docker-compose. This will setup a developement environment with PHP7-fpm, mysql and Nginx

## Structure
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
## Usage
clone this repository on your local or remote server, and follow below :
`docker-compose.yml` contains all your configurations you need. 
- 


