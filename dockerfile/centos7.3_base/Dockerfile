FROM shawnyan/docker:centos7.3.1611
MAINTAINER Shawn Yan https://github.com/shawn0915/docker-study

# vim wget sshd
RUN yum install -y vim* wget iproute net-tools unzip bc
RUN yum install -y openssh-server openssl
RUN echo 'centos7.3_base 2017-10-01' > /root/Readme.md
RUN sed -i 's/#PermitRootLogin yes/PermitRootLogin yes/g' /etc/ssh/sshd_config
RUN echo "root:password" | chpasswd

LABEL name="CentOS 7.3" \
    build-date="20171001"

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]