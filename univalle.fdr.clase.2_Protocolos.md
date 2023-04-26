---
id: xca663mkwp1tw27fyykc8ov
title: 2_Protocolos
desc: ''
updated: 1682140786418
created: 1681582133488
---

# Protocolos mas importantes en las capas

![](/assets/images/2023-04-15-13-41-09.png) 

# PDU segun la capa en el modelo TCP/IP

- Capa de aplicación: Mensaje
- Capa de transporte: Segmento (TCP) o Datagrama (UDP)
- Capa de red: Paquete
- Capa de enlace de datos: Trama

### Arquitecturas de aplicacion

- Cliente servidor : El cliente solicita un servicio al servidor
- Peer to peer (P2P) : Los clientes se comunican entre si
- Hibridos (cliente servidor y P2P) : Los clientes se comunican entre si y con el servidor (Napster, Mensajeria instantanea)

### Cliente servidor

**Servidor**: Computador siempre on, direccion ip permanente, servidores por escalamiento

**Cliente**: Se comunica con el servidor, puede ser intermitente la conexion, puede tener ip dinamicas, no se comunica entre clientes

### P2P 

Servidor no siempre alerta, sistemas terminales arbitrarios se comunican entre si, pares se conectan intermitentemente y cambian sus IP. Muy escalable.

### Protocolos de capa de aplicacion

- Definen los tipos de mensajes intercambiados
- SIntaxis de los tipos de mensajees
- Semantica de los tipos de mensajes
- Reglas para cuando y como los precesos envian o reciben mensajes

# Proceso 

Prgorama que corre en una maquina

- **Proceso Cliente** : Proeso que inicia la comunicacion
- **Proceso servidor** : Proceso que espera la comunicacion

## Sockets

Los procesos envian/reciben mensajes a/desde los sockets, que son **analogos a puertas**.Sirven para comunicar procesos en la misma maquina o en maquinas diferentes.

## Servicios de los protocolos de transporte

![](/assets/images/2023-04-15-14-01-13.png)