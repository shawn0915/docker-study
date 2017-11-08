FROM shawnyan/docker:centos7.3_systemd

# vim wget sshd openssl
#RUN yum install -y vim* wget iproute net-tools unzip bc
#RUN yum install -y openssh-server openssl
#RUN sed -i 's/#PermitRootLogin yes/PermitRootLogin yes/g' /etc/ssh/sshd_config
#RUN echo "root:password" | chpasswd

LABEL name="CentOS 7.3 v2" \
    build-date="20171108"

EXPOSE 22 80 8080 5601 9200

#CMD ["/usr/sbin/sshd", "-D"]