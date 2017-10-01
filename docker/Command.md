# 常用命令

- [docker build](dockerBuild.md)


> 基础命令
```bash
docker info
docker search
```

> 拉取镜像
```bash
docker pull
docker pull centos:7.3.1611
```

> 运行容器
```bash
# docker run
docker run --name centos7.3 -i -t centos:7.3.1611 /bin/bash
# --detach => -d
docker run --name centos7.3_d -i -t -d centos:7.3.1611 /bin/bash
# 自动重启
docker run --restart=always
```

> 容器交互
```bash
docker exec -t -i centos7.3 /bin/bash
```

> 查看镜像
```bash
docker images
docker images shawnyan/docker
docker image ls -a
docker image rm <CONTAINER ID>
docker image rm `docker image ls -a -q`
# 构建镜像的每一层
docker history <id>
```

> 启停容器
```bash
docker start centos7.3
docker stop centos7.3
docker restart centos7.3
```

> 删除容器
```bash
docker rm <CONTAINER ID>
docker rm `docker ps -a -q`
```

> 监控容器
```bash
docker ps
docker ps -a
docker container ls -a
#
docker stats centos7.3
docker logs centos7.3
docker logs -ft centos7.3
```

> 查看容器信息
```bash
docker inspect centos7.3
docker inspect centos7.3 --format='{{ .ID }}'
docker inspect centos7.3 --format='{{ .NetworkSettings.IPAddress }}'
docker inspect centos7.3 --format='{{ .State.Status }}'
```

> Docker ToolBox host ip
```bash
docker-machine ip
```

> 提交定制容器
```bash
docker commit -m "comment" <CONTAINER ID> <user/repo>
docker commit -m "centos7.3 core" -a "shawnyan" e819c4cb23a4 shawnyan/docker:centos7.3
#
docker push <user/repo:tag>
```
