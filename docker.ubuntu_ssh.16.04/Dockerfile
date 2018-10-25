# sshd
#
# VERSION               0.0.1

FROM     ubuntu:16.04
MAINTAINER Ray "zhangqinlei@gmail.com"

# make sure the package repository is up to date
RUN apt-get update

RUN apt-get install -y openssh-server sudo curl git zsh net-tools iputils-ping apt-utils vim byobu tzdata
RUN mkdir /var/run/sshd

RUN useradd -ms /bin/bash ray
RUN echo 'ray:123456' | chpasswd
RUN adduser ray sudo

RUN rm -rf /var/lib/apt

EXPOSE 22
CMD    ["/usr/sbin/sshd", "-D"]
