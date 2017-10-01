FROM shawnyan/docker:centos7.3_systemd
RUN yum install -y httpd; yum clean all; systemctl enable httpd.service
EXPOSE 80
CMD ["/usr/sbin/init"]