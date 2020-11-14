FROM ubuntu:latest

ARG PASSWORD

RUN apt update && apt install  openssh-server sudo -y

RUN  echo root:${PASSWORD} | chpasswd

RUN service ssh start

COPY ./ssh/.ssh/authorized_keys /root/.ssh/authorized_keys

COPY ./ssh/sshd_config /etc/ssh/sshd_config

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]
