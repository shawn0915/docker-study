# Docker

## check
[check-config](check-config.sh)

```bash
curl https://raw.githubusercontent.com/docker/docker/master/contrib/check-config.sh > check-config.sh
bash ./check-config.sh
```

## install
- [Install](Install.md)
- [post-install](https://docs.docker.com/engine/installation/linux/linux-postinstall/)


## 常用命令

运行容器
```bash
docker run -i -t ubuntu /bin/bash
```

命名容器
```bash
docker run --name demo_ubuntu -i -t ubuntu /bin/bash
```

启停容器
```bash
docker start demo_ubuntu
docker stop demo_ubuntu
docker restart demo_ubuntu
```


## userguide
[userguide](https://docs.docker.com/engine/userguide/)