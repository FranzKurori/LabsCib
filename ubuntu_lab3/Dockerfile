FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive


RUN apt update && apt install -y apache2 php libapache2-mod-php openssh-server curl


RUN mkdir /var/run/sshd && echo 'root:secreto123' | chpasswd
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config


RUN echo '<?php \
if(isset($_POST["usuario"])) { \
    echo "Intento de login recibido para: " . $_POST["usuario"]; \
} else { \
    echo "<form method=\"POST\"> \
    Usuario: <input type=\"text\" name=\"usuario\"><br> \
    Clave: <input type=\"password\" name=\"clave\"><br> \
    <input type=\"submit\" value=\"Enviar\"> \
    </form>"; \
} \
?>' > /var/www/html/index.php


RUN rm /var/www/html/index.html

EXPOSE 80 22


CMD service ssh start && apachectl -D FOREGROUND
