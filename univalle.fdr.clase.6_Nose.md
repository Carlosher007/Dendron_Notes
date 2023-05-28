---
id: byb3eqdsshvzqyvkfkn117i
title: 6_Nose
desc: ''
updated: 1684527502570
created: 1684527502570
---
Necistamos comunicacion entre host y cliente, por lo que necesitamos un adaptador de tipo fuente.

> En la maquina virtual, en  Red
> Ponemos en conectado a: Adaptador puente y legimos un nombre (el profe puso como que el cel)

Con ifconfig en la vm podemos ver una direccion ip al lado de inet. Esa direccion IP

Con ifocnfig o ipconfig en la maquina de nosotros podemos ver la ip

Para acceder al servidor de la vm desde el pc debemos pear la direcion ip en el navegador pero no se mostrara nd si no tiens un servidor corriendo

Verifica con systemctl status apache2.service para ver el estado de apache2
Lo encendemos com systemctl start apache2.service y verificamos que si funciona.

Si tengo archivos en el pc y quiero pasarlos a la vm veo si tengo un servidor ftp corriendo
Con apt-get install vsftpd instalamos el servicio
Con systemctl start vsftpd lo iniciamos

Con netstat -tulpm vemos lo dde los puertos.
Puedo conectarme a un cliente ftp.

En este caso usemos filezilla. En Host demo conectarme al servidor con la direccion IP (esto lo hacemos en el pc)
Ponemos en username kali y en password nuestra paswword. Le doy conectar. Lado izq pz lado derecho vm
en remote pnemos /var/... donde va lo de apache.

Vammos a la mv y revisamos archv de config: nano /etc/vsftpd.conf
Cambiamos lo siguiente para q ell server ftp empiece a funcionar: descomentamos el de write_enable=YES, el de local_enable=YES, el de local_umask=022, .lo de connect_from_port_20=YES es para el puerto y cambiarlo, el ftpd_banner es msg de banner, Pero antes hacmos control o y le damos otro nombre para hacer una copia. Y modificamos el original.
