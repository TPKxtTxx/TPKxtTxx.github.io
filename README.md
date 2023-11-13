Link de la Pagina: 
https://tpkxttxx.github.io

version: '3'

services:
  web:
    image: php:7.4-apache
    container_name: my-php-app
    volumes:
      - ./src:/var/www/html
    ports:
      - "8080:80"
    environment:
      MYSQL_HOST: db
      MYSQL_DATABASE: my_database
      MYSQL_USER: my_user
      MYSQL_PASSWORD: ${MYSQL_PASSWORD:-my_secret_password}

  db:
    image: mariadb:latest
    container_name: my-mysql-db
    volumes:
      - db_data:/var/lib/mysql
    environment:
      MYSQL_ROOT_PASSWORD: ${MYSQL_ROOT_PASSWORD:-root_password}
      MYSQL_DATABASE: my_database
      MYSQL_USER: my_user
      MYSQL_PASSWORD: ${MYSQL_PASSWORD:-my_secret_password}

volumes:
  db_data:
