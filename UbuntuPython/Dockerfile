ARG UBUNTU_VERSION=latest
ARG PYTHON_VERSION=3

FROM ubuntu:${UBUNTU_VERSION}

ENV DEBIAN_FRONTEND noninteractive

RUN apt update \
    && apt install -y openssh-server ssh sudo git vim \
    && apt install -y openssh-server ssh sudo git vim python${PYTHON_VERSION} \
    && useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 ubuntu \
    && echo "ubuntu:ubuntu" | chpasswd \
    && echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers \
    && service ssh start

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
