FROM python:3.7.6-stretch

RUN pip install pip --upgrade
RUN pip install ansible

RUN apt-get update -y && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    sshpass

# RUN ssh -o StrictHostKeyChecking=no root@10.5.0.4

# RUN ssh -o StrictHostKeyChecking=no root@10.5.0.3
COPY ./.ssh/ root/.ssh/

RUN chmod 600 -R /root/.ssh
RUN chown root /root/.ssh

RUN  eval "$(ssh-agent -s)"
RUN ssh-add ~/.ssh/id_rsa

RUN apt install -y rsync

WORKDIR /home/ansible/provisioning
