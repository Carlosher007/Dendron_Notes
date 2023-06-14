---
id: urga656qt5vk3pgi6lauqg7
title: 7_Capa_Transporte
desc: ''
updated: 1685584746491
created: 1685575246903
---

# La capa de trasnporte


## Proposito de la capa de traasnporte

Permite la segmetacion de datyos y brinda el control necesario para reensabmblar las partes dentro de los disitntos streams de comunicación.

Se crea con el concepto de segmentar los archivos. Casi todas las apps se segmentan menos las que son pequeñas. Ademas de segmentar armar los segmentos.

- Rastreo de comunicacion de quien envio y y quien recibio

## Multiplexacion

Este concepto tiene sentido en el contexto de redes convergentes (conocidas como redes de multiservicio). Es aquella que permite la prestacion de multiples servicios a traves del mismo enlace.

## Protocolos en la capa de trasnporte

> Si una aplicacion segmentos que los segmentosa deben llegar en una secuencia (orden) especifica debe **usar el protocolo TCP**. 

> Una aplicacion que puede tolerar cierta perdida de datos durante la trasnmision a traves de red (un videojuego o una conferencia) es por ejemplo **el protocolo UDP**

Una forma de saber cyual estamos usando es con el comando **netstal** o **wireshark**


**TCP**
- **Acuse de recibo**: Cuando el servidor por ejmplo recibe los datos los segmentos y envia un acuse de reciobo al pc por ejemplo de que recibio los segmentos.
- **Seguimiento de segmentos de datos transimitdos**: Tando el emisor como el receptor necesits saber cuanto sosn lsod atos que se envian o se reciben (se hace a traves de un Encambezado)
- **Retrasmision de cualquier dato sin acuse de recibo**, es decir, que si no llega el mensaje se retrasnmite

**UDP**
- No hay **acuse de recibo**, lo importante es que los datos lleguen  de forma rapida

## Encapsulacion

Consiste en agregar una cantidad de información  los fdatos que se van a atransimiterantes de transmitirlos a otra capa.

Este proceso se da entre capas y de esta manera la capa sabe que hacer con estos datos.

> Existen mas protocolos en la capa de trasnpoprte que solo el TCP y UDP

## Encabezados de tcp y udp

TCP utiliza 20 bytess para su encabezado

UDP utiliza 8 bytes para su encabezado

# Actividad

> Puetois del 0 al 1023 son los puertos bien conocidos (Los deifne la IANA)
> Puertos de 1024 a 49151 son puertos registros  
> Puerttos de 49152 a 65525 sopn puertos privados y o dinamicos (Cuando se inicia conexion, no se ha asignado direccion IP a usuario)


**Los protoclos UDP bien conocidos son el TFTP 69 (envia datgos sin hacer conexion)**

## UDP
Lado servidor
![](/assets/images/2023-05-31-20-16-49.png)
Lado cliente
![](/assets/images/2023-05-31-20-17-24.png)

Cual es el registro que relaciona el nombre del host con la direccion IP

Si al ahcer ping sale **Request time out** ers pq tiene desactivado el servicio ISMP para evitar dar repuestas de solicitudes que vvengan a ese puertto o pq no existe una ip para ese host.

Whois es para pasar de ip a hopst o nombre de host.

CAPA DE TRASNPORTE : 