FROM ubuntu:18.04
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y openssh-server apache2 vsftpd unattended-upgrades nano
EXPOSE 22 80 21
CMD service ssh start ; service apache2 start ; service vsftpd start ; tail -f /dev/null
