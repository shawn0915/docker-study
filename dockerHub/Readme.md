# Docker Hub

## official website

[hub.docker.com](https://hub.docker.com/)

## login

```bash
docker login
docker logout
```

## 私有仓库

在CentOS上安装docker-registry
```bash
docker run -d -e SETTINGS_FLAVOR=dev -e STORAGE_PATH=/tmp/registry -v /opt/data/registry:/tmp/registry  -p 5000:5000 registry
```
私有仓库位置：/opt/data/registry

可以把项目`https://github.com/docker/docker-registry.git`克隆到本地
