FROM ubuntu:latest

# Instalar dependencias necesarias
RUN apt update && apt install -y openssh-server libpam-google-authenticator sudo nano hydra

# Configurar el servicio SSH
RUN mkdir /var/run/sshd
RUN sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config


RUN useradd -m -s /bin/bash usuario2001 && echo 'usuario2001:qwerty' | chpasswd

EXPOSE 22

# Iniciar el servicio SSH en primer plano
CMD ["/usr/sbin/sshd", "-D"]
