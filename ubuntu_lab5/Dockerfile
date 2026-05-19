FROM ubuntu:22.04
ENV DEBIAN_FRONTEND=noninteractive


RUN apt-get update && apt-get install -y fail2ban rsyslog openssh-server iptables hydra


RUN mkdir -p /var/run/sshd && echo 'root:secreto123' | chpasswd
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config


RUN sed -i '/imklog/s/^/#/' /etc/rsyslog.conf
RUN echo "[sshd]\nenabled = true\nport = ssh\nlogpath = /var/log/auth.log\nmaxretry = 3\nbantime = 600\nbackend = polling" > /etc/fail2ban/jail.local

RUN touch /var/log/auth.log && chown syslog:adm /var/log/auth.log


CMD service rsyslog start; service fail2ban start; service ssh start; tail -f /dev/null
