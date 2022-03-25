FROM node:12.22-bullseye

MAINTAINER Cyris Tseng <gene26620560@gmail.com>

RUN \
    apt-get update && \
    apt-get install -y openssh-server && \
    mkdir /var/run/sshd && \
    sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin no/' /etc/ssh/sshd_config && \
    sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config && \
    sed -i 's/#PubkeyAuthentication yes/PubkeyAuthentication yes/' /etc/ssh/sshd_config && \
    sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config

WORKDIR /home/node
RUN echo 'node:nodenode' | chpasswd && \
    npm install -g hexo-cli && \
    mkdir hexo-site && \
    cd hexo-site && \
    hexo init


EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
