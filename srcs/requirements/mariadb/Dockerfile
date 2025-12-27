# A Docker container that contains only MariaDB, without nginx.
# Um contêiner Docker que contém apenas o MariaDB, sem nginx.

FROM alpine:bullseye

RUN apk update && apk add --no-cache mariadb mariadb-client \
	bash tini 

RUN mkdir -p /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d \
	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 

COPY ./conf/my.cnf /etc/my.cnf

COPY ./tools/init.sql /docker-entrypoint-initdb.d/