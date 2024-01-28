# Spring Boot with Oracle

Spring Boot with Oracle DB

ref: https://container-registry.oracle.com/ords/f?p=113:4:7017560529758:::4:P4_REPOSITORY,AI_REPOSITORY,AI_REPOSITORY_NAME,P4_REPOSITORY_NAME,P4_EULA_ID,P4_BUSINESS_AREA_ID:803,803,Oracle%20Database%20Express%20Edition,Oracle%20Database%20Express%20Edition,1,0&cs=34F4ZUpbk6kueA-wlN8oJ0ojpiff2eJ0iWh6Hupmx6ifnJ7ZHV64JzzNnz-PIRwHGJrIeeOGhs1KgUD0GO6iFSg

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
