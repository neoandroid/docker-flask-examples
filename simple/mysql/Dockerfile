FROM mysql:5.7
MAINTAINER Jordi Miguel <jordi.miguel.torrent@gmail.com>

COPY sql.sql /docker-entrypoint-initdb.d/

EXPOSE 3306
CMD ["mysqld"]
