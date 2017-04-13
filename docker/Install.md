# Install

https://docs.docker.com/engine/installation/

* CentOS

https://store.docker.com/editions/community/docker-ce-server-centos?tab=description

* Prerequisites

Docker CE is supported on CentOS 7.3 64-bit.

1. Set up the repository

Set up the Docker CE repository on CentOS:

```
sudo yum install -y yum-utils

sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

sudo yum makecache fast
```


> https://download.docker.com/linux/centos/7/x86_64/stable/Packages/

2. Get Docker CE

Install the latest version of Docker CE on CentOS:

```
sudo yum -y install docker-ce
```

Start Docker:

```
sudo systemctl enable docker
sudo systemctl start docker
```


3. Test your Docker CE installation

Test your installation:

```
sudo docker run hello-world
```


