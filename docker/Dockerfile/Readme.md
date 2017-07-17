## Dockerfile-c7-systemd

```bash
docker build --rm -t local/c7-systemd .

docker run -ti local/c7-systemd /bin/bash
```

## Dockerfile-c7-systemd-httpd
```bash
docker build --rm -t local/c7-systemd-httpd .

docker run -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro -p 80:80 local/c7-systemd-httpd
```

## Dockerfile-c7-systemd-ssh
```bash
docker build --rm -t local/c7-systemd-ssh .

docker run -d -p 2222:22 --name sshtest local/c7-systemd-ssh
```
