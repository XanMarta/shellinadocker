FROM phusion/baseimage:master

RUN apt update -y

RUN apt install -y openssl shellinabox sudo

RUN mkdir -p /etc/my_init.d

COPY script.sh /etc/my_init.d/siab.sh

RUN chmod +x /etc/my_init.d/siab.sh

EXPOSE 8000

RUN useradd -m -s /bin/bash user && usermod -aG sudo user

RUN echo user:password | chpasswd
