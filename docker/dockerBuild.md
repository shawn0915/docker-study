# docker build

## centos

- centos7.3.1611
```bash
cd centos7.3.1611
docker build --rm -t="shawnyan/docker:centos7.3.1611" .
docker build --rm --no-cache=true -m=2g --memory-swap=4g -t="shawnyan/docker:centos7.3.1611_2m" .
```

- centos7.3_base
```bash
cd centos7.3_base
docker build --rm -t="shawnyan/docker:centos7.3_base" .
```

- centos7.3_systemd
```bash
cd centos7.3_systemd
docker build --rm -t="shawnyan/docker:centos7.3_systemd" .
#
docker run -dit --privileged=true --name centos7 shawnyan/docker:centos7.3_systemd
# httpd
docker run -dit --privileged=true --name httpd -v /Volumes/HDD/dockerdata:/data:rw -p 8080:80 shawnyan/docker:centos7_v2
``` 

- centos7.3_systemd_httpd
```bash
cd centos7.3_systemd_httpd
docker build --rm -t="shawnyan/docker:httpd" .
#
docker run --privileged=true -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro -p 80:80 shawnyan/docker:httpd
# mac
docker run -dit --privileged=true -p 8080:80 --name httpd shawnyan/docker:httpd
``` 

## ubuntu

- ubuntu16.04_sshd
```bash
cd ubuntu16.04_sshd
docker build --rm -t="shawnyan/docker:ubuntu16.04_sshd" .
#
docker run -d -it <id>
```

## oraclelinux

- ol7_mysql57
```bash
# build
docker build --rm --no-cache=true -t "shawnyan/docker:mysql57" .
# run
#docker run --name my-container-name -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql/mysql-server:tag
docker run --name mysql57 -p 33306:3306 -e MYSQL_ROOT_PASSWORD=password -d shawnyan/docker:mysql57
# connect
docker exec -it mysql57 mysql -uroot -p
```