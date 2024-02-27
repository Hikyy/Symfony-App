FROM mariadb:latest

ENV MYSQL_ROOT_PASSWORD=password
ENV MYSQL_DATABASE=symfony_db

COPY ../../database/init.sql /docker-entrypoint-initdb.d/
