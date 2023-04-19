---
id: 6tl17ykgcgvx2ylyg9lcjhd
title: 3_ConexionConSwitch
desc: ''
updated: 1680717633033
created: 1680095476365
---

# Parte 1 : Explorar IOS mediante CLI

- Conecte el PC1 a S1 mediante un cable de consola
- Establezca una sesion de terminal con el S1
- Examine la ayuda IOS
  -  Se puede usar el `?` o escribir un comando existente como `ssh` y luego el `?` para ver sus opciones.
-  Ingrese al modo EXEC privilegiado
   -  `enable`
- Ingrese en el modo de configuraciòn global
  - `configure terminal`
- Examine el archivo de configuracion actual del switch
  - Primero fui al modo privilegiado con `end`y luego `show running-config`

# Parte 2: Configuracion de parametros basicos de un switch

- Asigne un nombre a un switch
  - `hostname S1`
- Proporcione acceso seguro a la linea de consola con una contraseña
  - `line console 0` `password cisco` `login`
- Verifique que el acceso sea seguro
- Proporcione acceso seguro al modo privilegiado, usando una contraseña privilegiada y usando su codigo
  - `conf t` `enable secret 212553`
- Veriffique el que acceso al modo privilegiado sea seguro
- Encripte las contraseñas de consola y enable
  - `conf t` `service password-encryption`
- Configure un aviso del mensaje del día (MOTD)
  - `banner motd *Bienvenido a la red de la Universidad del Valle*`
- Examine el archivo de configuracion actual del switch
  - `show running-config`
- Guarde el archivo de configuracion
  - `copy running-config startup-config` o `wr`
- Examine el archivo de configuracion guardado (esta en la memoria NVRAM)
  - `show startup-config`

# Configuracion de interface de administracion de un switch

- Realice las conexiones ethernet
- Configure el direccionamiento de PC1 Y PC2 en el packet tracer: Asignar una IP y una mascara de sub red a cada PC
- Realice una prueba de ping entre los 2 PCS
  - Desde la PC1, abra la línea de comandos. Escriba el comando "ping" seguido de la dirección IP de la PC2.
- ¿Podria hacer ping a los switch? ¿Por que? No, porque los switches no tienen direcciones IP asignadas en las interfaces que estan conectadas a las PCs.
- Verifique la tabla MAC de S1
  - `show mac address-table` 
- Configure y habilite el S1  con una direccion IP (vlan1)
  - Estango en la configuracion global escribimos: `interface vlan 1` `ip address 192.168.75.250 255.255.255.0` `no shutdown` Siendo en ip adress primero la ip y luego la mascara de subred.
- Examine el archivo de configuracion acutal del switch
  - `show running-config`
- Verifique al configuracion de direcciones IP en el S1
  - `show ip interface brief`
- Quite el cable de consola
- Realice una prueba de ping desde PC1 a S1
  - Desde la PC1, abra la línea de comandos. Escriba el comando "ping" seguido de la dirección IP del S1.
- Repita para S2
- Realice una conexion remota a S1 desde PC1 usando TELNET
  - Usando `telnet ip`no obtenemos respuesta pues primero hay que definir las conexiones virtuales en el switch
- Configure una clave Class123 en las lineas VTY para acceso remoto, purbee nuevamente con el protocolo TELNET
  - En configuracion gloabl de la terminal (volviendo a conectar el cable de consola) escribimos: `line vty 0 5` `password Class123` `login` . Luego en el Comand Prompt del PC y haber eliminado el cable de consola escribimos `telnet ip` y nos pide la contraseña que definimos.




