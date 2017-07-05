# Docker LEMP Microservices
This is a LEMP stack infrastructure on docker. 

### Microservices -
* nginx 1.13.1
* mysql 5.6
* php-fpm 5.6

### Pre-requisites
You must have Docker installed. Check the Installation [Guide](https://docs.docker.com/engine/installation/).

### Setup
1. Copy the PHP project into the docroot folder.
2. Build the docker infrastructure `docker-compose build`
3. Run `docker-compose build up -d`
4. Open the link [http://localhost:8080/](http://localhost:8080/).


### Database Configuration
* HOST: mysql
* PORT: 3306
* USERNAME: root
* PASSWORD: root@mysqlserver (update password in mysql dockerfile)




