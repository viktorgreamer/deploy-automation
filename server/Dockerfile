FROM ubuntu:latest

ARG PASSWORD

RUN apt update && apt install  openssh-server sudo -y

RUN  echo root:${PASSWORD} | chpasswd

RUN service ssh start

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]
