FROM ubuntu:16.04
MAINTAINER Shawn Yan https://github.com/shawn0915/docker-study
ENV REFRESHED_AT 2017-10-01

RUN apt-get update
RUN apt-get install -y openssh-server vim
RUN sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config
RUN mkdir /var/run/sshd
RUN echo "root:password" | chpasswd

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]