---
id: 4vhp92zlp8zu10ey217meoq
title: 5_FTP
desc: ''
updated: 1683164818436
created: 1683162867346
---

Permite conectar a un cliente con un servidor con el proposito de transferir archivos a /desde el host remoto. Por ejemplo para subir archivos  a un servidor web.

Sigue el modelo cliente servidor, utiliza TCP, puerto 21 para control y 20 para datos (transferencia).

Recordemos que el cliente es el sitio que inicia la conexion (**ya sea a/desde el sitio remoto**) y el servidor es el sitio que escucha y acepta la conexion siendo el **host remoto**.

Utiliza el protocolo de transporte TCP. 

FTP es un protocolo que asigna permisos a un usuario para escribir o leer y descargar archivos de una carpeta de un servidor remoto.

## Para hacer que funcione

Con `netstat - tulpn` podemos ver los puertos que estan escuchando en el servidor.

Para que funcione debemos instalar el servidor ftp y luego ponerlo a corre en el puerto 21, pues este puerto es para el control.

Para instalar en arch linux se utiliza `pacman -S vsftpd`. Vsftpd es el servidor ftp.

## Vsftpd

Ahora necessitamos correlo con `systemctl start vsftpd`. Y para que se inicie automaticamente al iniciar el sistema es con `systemctl enable vsftpd`.

Para saber si funciono es con `systemctl status vsftpd`.

Para conectarme desde el cliente a ese servidor es con la ip, la cual la consulto con ifconfig. 

Si nos conectamos sin mas no se puede, pues no hemos creado un usuario. Para crear un usuario es con `useradd -m -d /home/usuario -s /bin/bash usuario`. El -m es para crear el directorio home, el -d es para especificar el directorio home, el -s es para especificar el shell.

> En el servidor ftp es necesario crear un usuario.

## Clientes FTP

Existen varios, entre ellos: Cyberduck, Filezilla, WinSCP, etc.

### Cyberduck

