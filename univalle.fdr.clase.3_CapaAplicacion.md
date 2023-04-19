---
id: eaoqzv722b7zzifwm7nagxo
title: 3_CapaAplicacion
desc: ''
updated: 1681595064467
created: 1681587065145
---

# Diferencia entre modelo OSI y TCP/IP

**Modelo OSI** s un modelo de referencia que se utiliza para describir cómo las aplicaciones de red se comunican entre sí a través de una red. Este modelo se divide en siete capas: física, de enlace de datos, de red, de transporte, de sesión, de presentación y de aplicación. Cada capa tiene un conjunto específico de funciones y protocolos que se utilizan para asegurar una comunicación eficiente y fiable.

**TCP/IP** es un modelo de referencia que se utiliza para describir cómo las aplicaciones de red se comunican entre sí a través de una red. Este modelo se divide en cuatro capas: capa de aplicación, capa de transporte, capa de red y capa de enlace de datos. Cada capa tiene un conjunto específico de funciones y protocolos que se utilizan para asegurar una comunicación eficiente y fiable.

# Modelo ISO/OSI

### Capas de modeloosi

-**Aplicación**: Proporciona servicios a los usuarios para el intercambio de datos
-**Presentación**: Permite que las aplicaciones interpreten el significado de los datos
-**Sesión**: Permite que las aplicaciones se comuniquen. SIncronizacionm recuperacion de errores, etc.
-**Transporte**: Permite que los dispositivos finales se comuniquen. TCP, UDP
-**Red**: Permite que los dispositivos finales se comuniquen en redes diferentes. IP
-**Enlace de datos**: Permite que los dispositivos finales se comuniquen en una misma red. Ethernet, Token Ring, FDDI, etc.
-**Fisica**: Permite que los dispositivos finales se comuniquen a traves de un medio de transmision. Cable de cobre, fibra optica, ondas de radio, etc.


# Capas modelo TCP IP

![](/assets/images/2023-04-15-16-26-35.png)

## Protocolos Data Unit (PDU)

![](/assets/images/2023-04-15-16-27-04.png)

## Servicios de los protoclos de trasnsporte de la capa de aplicacion

- Servicio TCP
- Servicio UDP

# Web y HTTP

Servicio mas popular de internet basado en la arquitectura cliente-servidor, donde cada objeto es accesible a traves de una URL.

Es modelo cliente servidor donde el **cliente** es el browser que requiere, recibe o despliega objetos y el **servidor** es el servidor web que envia objetos en respuesta a las solicitudes del cliente.

> HTTP es un **protocolo de la capa aplicacion de la web**

# HTTP 1.0

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