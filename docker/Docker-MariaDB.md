# MariaDB Docker


## docker-mariadb-10.1

```bash
# pull
docker pull mariadb:10.1
# run
docker run --name mariadb101 -p 33326:3306 -e MYSQL_ROOT_PASSWORD=password -d mariadb:10.1
# connect
docker exec -it mariadb101 mysql -uroot -p
```

## docker-mariadb-10.2

```bash
# pull
docker pull mariadb:10.2
# run
docker run --name mariadb101 -p 33336:3306 -e MYSQL_ROOT_PASSWORD=password -d mariadb:10.2
# connect
docker exec -it mariadb101 mysql -uroot -p
```

## REF

- [docker-library/mariadb](https://github.com/docker-library/mariadb)
- [dockerhub/mariadb](https://hub.docker.com/_/mariadb/)