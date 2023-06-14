---
id: y8j92hfarof1y5ee1qj0nj4
title: 8_Capa_Red
desc: ''
updated: 1686188478644
created: 1686181267725
---

# Capa de red

> Link: https://www.sapalomera.cat/moodlecf/RS/1/course/module6/index.html#6.0.1.1

# Como funciona

La capa de red, o la capa 3 de OSI, proporciona servicios que permiten que los dispositivos finales intercambien datos a través de la red. Para lograr este transporte de extremo a extremo, la capa de red utiliza cuatro procesos básicos:

- Direccionamiento de dispositivos finales: de la misma manera en que un teléfono tiene un número telefónico único, los dispositivos finales deben configurarse con una dirección IP única para su identificación en la red. Un dispositivo final con una dirección IP configurada se denomina “host”.

- Encapsulación: la capa de red recibe una unidad de datos del protocolo (PDU) de la capa de transporte. En un proceso denominado “encapsulación”, la capa de red agrega la información del encabezado IP, como la dirección IP de los hosts de origen (emisor) y de destino (receptor). Una vez que se agrega la información de encabezado a la PDU, esta se denomina “paquete”.

- Enrutamiento: la capa de red proporciona servicios para dirigir los paquetes a un host de destino en otra red. Para que el paquete se transfiera a otras redes, lo debe procesar un router. La función del router es seleccionar las rutas para los paquetes y dirigirlos hacia el host de destino en un proceso conocido como “enrutamiento”. Un paquete puede cruzar muchos dispositivos intermediarios antes de llegar al host de destino. Cada ruta que toma el paquete para llegar al host de destino se denomina “salto”.

- Desencapsulación: cuando un paquete llega a la capa de red del host de destino, el host revisa el encabezado IP del paquete. Si la dirección IP de destino en el encabezado coincide con su propia dirección IP, se elimina el encabezado IP del paquete. Este proceso de eliminación de encabezados de las capas inferiores se conoce como “desencapsulación”. Una vez que la capa de red desencapsula el paquete, la PDU de capa 4 que se obtiene como resultado se transfiere al servicio correspondiente en la capa de transporte.

A diferencia de la capa de transporte (capa 4 de OSI), que administra el transporte de datos entre los procesos que se ejecutan en cada host, los protocolos de la capa de red especifican la estructura y el procesamiento de paquete que se utilizan para transportar los datos desde un host hasta otro. Operar sin tener en cuenta los datos transportados en cada paquete permite que la capa de red transporte paquetes para diversos tipos de comunicaciones entre varios hosts.

# Para esto se utiliza los protocolos de internet IPv4 y IPv6

## Cracteristicas del protoclo IP

> Encapsulamientoi de IP
Los segmentos se encapsulan 
COnvertir los ddatagramas o segmentos en paquetes y los paquetes son datos que contienen ip de destino y d eorigne y dentro otro directorioq ue contiene un datagrama o segmento dependiendo del de tranporte

> Sin conexion: 
- El emisor  no sabe si el receptor esta escuchando o si el msg llego a tiempo
- El receptor no sabe que estan llegando datos

> Entrega por mejor esfuerzo (no confiable en sentido de que no se sabe si los parqutes llegaran)
- No se efectuen garantias de entrega
- LOs paquetes se enrutan velozmente a traves de la red
- Algunos paquetes se pueden perderse

> Independiente de los medios
- Los paquetes IP pueden viajar por diferentes tipos de medios

![](/assets/images/2023-06-07-19-08-37.png)

# IpV4
Se utiliza desde 1983 cuiando se impleento en la ARPANET Advanced Research Project Agency networl,m que fue precursora de Internet. 
Es un protoclo que ha evolcuionado poco en la manera de como funciona.

# Campos importantes del encabezado IPv4 (o icnluso IPV6)

> **Version:** CIOontiene un valor binario de 4 bits identica a la version del paquete IP. Para IPV4 es 0100, para IPV6 es 0110
> **Servicios diferenciados (DS):** Son los que permiten que hagamos tiempo de diseño de una apliacion la quality que esperamos d eun determinado programa, pues podemos poner en ese apartado el tipo de dato que estamos envinado y tambien si queremos que persistan mucho en la red. Los primeros 6 bits idetntifican el valor del putno de codigo diferenciados y los otros 2 bits identifican el valor de notificacion explicita.
> **Tiempo de vida (TTL):** Valor binario de 8 bits que se utiliza para limitar la vidsa util de un paquete. IMpiortante pq contiene el tiempo que el paquete puede andar por internet para llegar.No se establece en tiempo como tal, si no en cantidad de saltos
> **Protocolo:** Valor Binario de 8 bits que indica el tipo de contenido de datos que trasnporta el paquete ( el tipo de contenido de dartos de la capa de trasnporte).
> **Direccion IP de origen:**Valor binario de 32 bits que reprecenta la direccion IP de orgien del paquete
> **Direccion IP de destino:**Valor binario de 32 bits que reprecenta la direccion IP de destino


Cuandfo se debe fragmentar un paquete cuando apsa de un router a otro: **Cuando el paquere pasa de un enlace mas rapido a otro, o cuando tiene un mtu mas pqueño**

**MTU** determina cual es paquete mas pequeño

# ICMP es un protoclo diferente a TCP o UDP
ICMP es un protoclo que funciona en capa de red y trasnporte (se encarga de realziar las solicitude sy conexiones con los diferntes hsot para esperar una repsuesta)

Linux **tracerroute** y en windows **tracer**: **traceroute google.com**

**dhclient** es: 
**dhclient -v** es: 

**tracert ip** te da cuantos saltos se dan

![](/assets/images/2023-06-07-19-52-18.png)
 
# IPV6
Surge por el agotamiento de direcciones ip de ipv4
tiene expansion de la tabla de enrrutamiento de itnernet
falta de conewctividad extemo a extremo



Calcilño dos a la tres es 8, es decir que con 3 bits tengo la psibilidad de asingar 8 direccione sip de las cuales dos son reservadas y me quegan 6.

Con 2 bits puedo asignar dos computadores, con 3 bits puedo asignar 6 computadores.


**VER 8.1 PARA VE RCOMO ASINGA AVALOR BINARIO A LETERA**