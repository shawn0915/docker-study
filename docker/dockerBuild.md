# docker build

## centos

- centos7.3.1611
```bash
cd centos7.3.1611
docker build --rm -t="shawnyan/docker:centos7.3.1611" .
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
``` 

- centos7.3_systemd_httpd
```bash
cd centos7.3_systemd
docker build --rm -t="shawnyan/docker:centos7.3_systemd_httpd" .
#
docker run --privileged=true -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro -p 80:80 shawnyan/docker:centos7.3_systemd_httpd
``` 

## ubuntu

- ubuntu16.04_sshd
```bash
cd ubuntu16.04_sshd
docker build --rm -t="shawnyan/docker:ubuntu16.04_sshd" .
#
docker run -d -it <id>
```
