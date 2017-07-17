# Install

https://docs.docker.com/engine/installation/

* CentOS

https://store.docker.com/editions/community/docker-ce-server-centos?tab=description

* Prerequisites

Docker CE is supported on CentOS 7.3 64-bit.

1. Set up the repository

Set up the Docker CE repository on CentOS:

```
sudo yum install -y yum-utils device-mapper-persistent-data lvm2

sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

sudo yum makecache fast
```

Ref:
- [install-using-the-repository](https://docs.docker.com/engine/installation/linux/docker-ce/centos/#install-using-the-repository)
- [download-centos-7-pkg](https://download.docker.com/linux/centos/7/x86_64/stable/Packages/)

```bash
wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-selinux-17.03.2.ce-1.el7.centos.noarch.rpm
wget http://mirror.centos.org/centos/7/extras/x86_64/Packages/container-selinux-2.9-4.el7.noarch.rpm
```

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


