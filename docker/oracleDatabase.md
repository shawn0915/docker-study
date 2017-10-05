# Docker-OracleDatabase

- [oracle/docker-images/OracleDatabase](https://github.com/oracle/docker-images/blob/master/OracleDatabase/)

## 11.2.0.2 xe

! swap space 需要大于2048M

拉取基础镜像
```bash
docker pull oraclelinux:7-slim
```

下载xe安装包
```html
http://download.oracle.com/otn/linux/oracle11g/xe/oracle-xe-11.2.0-1.0.x86_64.rpm.zip
```

定制镜像
```bash
cd oracleDatabase/dockerfiles
./buildDockerImage.sh -v 11.2.0.2 -x
```