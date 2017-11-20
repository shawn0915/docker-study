# mysql-docker


## ol7_mysql56

```bash
# build
docker build --rm --no-cache=true -t "shawnyan/docker:mysql56" .
# run
docker run --name mysql56 -p 33316:3306 -e MYSQL_ROOT_PASSWORD=password -d shawnyan/docker:mysql56
# connect
docker exec -it mysql56 mysql -uroot -p
```

## ol7_mysql57

```bash
# build
docker build --rm --no-cache=true -t "shawnyan/docker:mysql57" .
# run
#docker run --name my-container-name -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql/mysql-server:tag
docker run --name mysql57 -p 33306:3306 -e MYSQL_ROOT_PASSWORD=password -d shawnyan/docker:mysql57
# connect
docker exec -it mysql57 mysql -uroot -p
```


## REF

- [mysql-docker](https://github.com/mysql/mysql-docker/MySQL-docker.md)
- [linux-installation-docker](https://dev.mysql.com/doc/refman/5.7/en/linux-installation-docker.html)