# Spring Boot with Oracle

Spring Boot with Oracle DB

## Setup Oracle DB using Docker

```shell
docker run -d --name oracle-db \
 -p 1521:1521 -p 5500:5500 \
 -e ORACLE_PWD=password \
 container-registry.oracle.com/database/express:21.3.0-xe

docker exec -it oracle-db sqlplus / as sysdba

CREATE USER SPRINGBOOT IDENTIFIED BY password

GRANT ALL PRIVILEGES TO SPRINGBOOT;
```
