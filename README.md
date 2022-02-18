# Laravel and Apache with Docker

## Instalation
1. Install Docker in your machine:
https://docs.docker.com/engine/install/ubuntu/

2. Clone this repository:

```
git clone https://github.com/renanorodrigues/docker-laravel.git
```
3. Enter in the directory of the project and open the terminal

4. Make sure to create a file named .env to input your database credentials
  POSTGRES_PASSWORD for your password in PostgreSQL
  POSTGRES_DB for the name of your database

### Build the image
Now is necessary to execute this command to build the image for container PHP-Apache
```
docker-compose up -d --build
```

### Create the project Laravel
It's necessary to run one command in terminal's container PHP to create the project in dir src.
So execute the bash in container PHP:
```
docker-compose exec php-apache /bin/bash
```
Finally, run the command to create the project:
```
composer create-project laravel/laravel .
```

### Localhost
Click in this link to view your project:  
http://localhost:8080/
