---
id: eaoqzv722b7zzifwm7nagxo
title: 4_CapaAplicacion
desc: ''
updated: 1683162859112
created: 1681587065145
---

# Que es la capa de aplicación

Se encarga de proporcionar servicios y protocolos para que las aplicaciones puedan comunicarse a través de la red.

# Ejemplo de la capa de aplicación

Un ejemplo común de una aplicación de red es el correo electrónico. Cuando envías un correo electrónico, tu programa de correo electrónico utiliza protocolos de la capa de aplicación, como SMTP (Simple Mail Transfer Protocol) para enviar el correo electrónico a través de la red hasta el servidor de correo electrónico de destino

Otro ejemplo es el protocolo HTTP (Hypertext Transfer Protocol) utilizado por los navegadores web. Cuando visitas un sitio web, tu navegador envía una solicitud HTTP al servidor web que aloja el sitio. El servidor web utiliza el protocolo HTTP para responder con la página web solicitada, que tu navegador luego muestra en tu pantalla.

# PDU de la capa de aplicación

La PDU de la capa de aplicación se llama mensa

Un mensaje de la capa de aplicación es una unidad de información que contiene los datos que una aplicación desea enviar a otra aplicación. Por ejemplo, en el caso de un correo electrónico, un mensaje podría contener el texto del correo electrónico, así como cualquier archivo adjunto. En el caso de una transferencia de archivo, el mensaje podría contener el archivo completo que se está transfiriendo.

# Web y HTTP

Servicio mas popular de internet basado en la arquitectura cliente-servidor, donde cada objeto es accesible a traves de una URL.

Es modelo cliente servidor donde el **cliente** es el browser que requiere, recibe o despliega objetos y el **servidor** es el servidor web que envia objetos en respuesta a las solicitudes del cliente.

> HTTP es un **protocolo de la capa aplicacion de la web** 

## Tiempo de respuesta o Round trip time

Tiempo ocupado en enviar un paquete pequeño desde el cliente al servidor y su regleso.

## Tipos de mensajes HTTP

> Requerimiento

Son mensajes que solicitan un recurso al servidor, por ejemplo un GET, POST, PUT, DELETE, etc.

> Respuesta

Son mensajes que envia el servidor en respuesta a una solicitud del cliente, por ejemplo un 200, 404, 500, etc.

## Las cookies

Son archivos de texto que se almacenan en el disco duro del cliente y que contienen informacion sobre el usuario.

Puede almacenar autorizacion, shopping carts, sugerencias, estado de la sesion del usuario...

## Web Caches o servidor proxy

Son servidores que almacenan copias de los objetos mas solicitados por los clientes. Satisfacen el requerimiento del cliente si involucrar al servidor destino.

## Https

Se usa con el SSL o Secure Socket Layer para encriptar la informacion que se envia entre el cliente y el servidor. En el puerto TCP 443.

# Apache

Es un servidor web de codigo abierto que usaremos para la capa de aplicacion del modelo, en sentido de que funcione para el cliente y el servidor.

## Dos puertos

Corre en los puertos 80 y 443. El puerto 80 es para cuando no es seguro. Mientras que el puerto 443 es el seguro.

## Transaccion

Solicita una peticion y recibe una respuesta.

# Tutorial Kali

Esocgemos Kali y no otra pq ya vienen herramientas

- Entramos como root
- `apt-get update`
- `apt-get install apache2` 

Ya instalamos apache 2 pero aun no se ha subido. Con el comando `netstat` podemos escanear un servidor o un sistema en busqueda de saber cuales puertos esta abiertos. Con el comando `netstat -tulpn` podemos ver los puertos que estan abiertos. 
Cuando escribimos `netstat -tulpn` y tenemos apache en servicio aparece 0::80. El 0 es la ip del servidor y el 80 es el puerto. 

Podemos entrar en el navegador escribiendo `127.0.0.1` y nos aparece la pagina de apache.

Por otro lado, con `systemctl status apache2` podemos ver el estado del servidor apache2. 

Con `systemctl start apache2` podemos iniciar el servidor apache2.

Para pararlo es con `systemctl stop apache2`. Y para reiniciarlo es con `systemctl restart apache2`.

## Apache en Kali

cd /, cd var, cd www/html, ls

Encontramos el index.html. Lo abrimos con `nano index.html` y lo editamos. Este archivo es el que se muestra en el navegador cuando entramos a la ip del servidor.

Ahora en el navegador podemos ir a `127.0.0.1/index3.html` y nos muestra el archivo index3.html si es que lo tenemos.

## Wireshark

SIrve para capturar todos los paquetes que vayan por la red. Puedo filtar por `tcp.port==80` para ver solo los paquetes que van por el puerto 80.


# Red en una maquina virtual

El adaptador de puente permite hacer un puente de conexion entre dos puentes, con el fin de poder acceder a la maquina virtual desde ele SO anfitrion. De este modo podemos hacer ping de la ip de la maquina virtual desde el anfiltron. 


## Cual es la diferencia entre una conexion NAT y Adaptador de puente en la maquina virtual