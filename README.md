#lab1
En este laboratorio se puso en práctica una técnica que fortalece la integridad de los datos, y el no repudio. Primero, porque mediante la herramienta de sha256sum, se genera un hash único para un archivo, y ese hash depende de los contenidos del mismo, por lo que, si se cambia el más minúsculo de los datos en el archivo, el hash generado será completamente distinto. De igual forma, con la herramienta openssl, se posee la capacidad de generar una firma digital única mediante criptografía para una versión del archivo, a partir de la llave privada del autor, y de igual manera, a partir de la llave privada, se generan llaves públicas para los destinatarios del archivo, que verificarán que el archivo mantuvo su integridad desde que fue enviado, hasta ser recibido. 
[Primera imagen](ubuntu_lab1/imagenes/lab1.1.png)
[Segunda imagen](ubuntu_lab1/imagenes/lab1.2.png)
[Tercera imagen](ubuntu_lab1/imagenes/lab1.3.png)
[Cuarta imagen](ubuntu_lab1/imagenes/lab1.4.png)
[Quinta imagen](ubuntu_lab1/imagenes/lab1.5.png)
[Sexta imagen](ubuntu_lab1/imagenes/lab1.6.png)
[Séptima imagen](ubuntu_lab1/imagenes/lab1.7.png)
[Octava imagen](ubuntu_lab1/imagenes/lab1.8.png)

##lab2
En este laboratorio se explora el uso de la autenticación multifactor, que otorga más seguridad frente a ataques de fuerza bruta o de diccionario especialmente. Como se ve en el laboratorio, un atacante pudo entrar al servidor ssh de un usuario fácilmente mediante un ataque de diccionario, sin embargo, cuando se implementó la MFA, el mismo ataque resultó en un intento fallido. 
[Primera imagen](ubuntu_lab2/imagenes/lab2.1.png)
[Segunda imagen](ubuntu_lab2/imagenes/lab2.2.png)
[Tercera imagen](ubuntu_lab2/imagenes/lab2.3.png)
[Cuarta imagen](ubuntu_lab2/imagenes/lab2.4.png)
(Aquí se cambió el diccionario de Rockyou.txt al que se muestra en la imagen, porque igual contiene la contraseña de prueba “qwerty” con solo 20 entradas, por lo que es más rápido en completar el ataque)
[Quinta imagen](ubuntu_lab2/imagenes/lab2.5.png)

###lab3
En este laboratorio, se demostró cómo un atacante puede espiar posibles datos sensibles a través de la red, con herramientas como Wireshark, especializadas en “sniffing”. Para contrarrestar esta amenaza, se formó un túnel ssh cifrado entre el emisor y el receptor de los datos. Este túnel permite que los datos viajen de forma segura, pues, aunque el atacante espíe los datos salientes, este los verá de forma cifrada, incapaz de saber el contenido original o tipo de datos de estos. 
[Primera imagen](ubuntu_lab3/imagenes/lab3.1.png)
[Segunda imagen](ubuntu_lab3/imagenes/lab3.2.png)
[Tercera imagen](ubuntu_lab3/imagenes/lab3.3.png)
[Cuarta imagen](ubuntu_lab3/imagenes/lab3.4.png)
[Quintaimagen](ubuntu_lab3/imagenes/lab3.5.png)