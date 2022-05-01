FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt update \
    && apt install -y openssh-server ssh sudo git \
    && useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 ubuntu \
    && echo "ubuntu:ubuntu" | chpasswd \
    && service ssh start

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
