FROM mariadb:11.4.1-rc
ENV MYSQL_DATABASE: symfony
ENV MYSQL_ROOT_PASSWORD: root
ENV MYSQL_ROOT_: root
COPY ../../database/init.sql /docker-entrypoint-initdb.d/
