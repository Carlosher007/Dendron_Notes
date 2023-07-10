---
id: a64t24ypt14ssftoc6ijzcg
title: 10_Siguiendo
desc: ''
updated: 1687396735369
created: 1687389224135
---

> Para aquellos que hagan el curso de ciberseguirdad de cisco tienen puntos extras

# Protocolo IPV6 (hexadecimal)
Empaquetar infromaicon y enviarla a traves de los routers.

# Que cambia respecto a ipv4
- LImite de salto
- identfiicador de flujo (nuevo)
- ...

# Version
0110

# ENcabezado
- Clase de trafico : protoclo
- LOngitud de contenido : longitud del paquete
- Siguiente protoclo: Protcolo de trasnporte utilizado
- LImite de salto: Saltos antes de ser eliminaod o cancelado (Ya no es tiempo total de expriacion)

# Como identificar entre ipv4 e ipv6 si estan en la misma red

> Para poder tenerlos en la misma red es necesario que el host lo tenga configurado.

## Saber si mi host tiene para ese protocolo

`ipconfig /all`

# Coexistencia entre ipv4 e ipv6

## Doble pila (tanto en enrutador como pc)
Tener habilitado ambos protcolos activados en la tarjeta de red.

> Mayor consumo
> Mayor esfuerzo para el administrador (cognitiva y tiempo)

## Tueelizacion
Meter paquetes IPV6 en una red que solo trasnporta ipv4 en un protocolo ipv4

## Traduccion
Un paquete piv6 traduce un paquete ivp4 y al reves. Se puede conseguri con un **Router NAT64**. 


# Icmp
Estabelcecer diagnositcios de los hosts y confimacion de algo

## ICMPv4 y ICMPv6 tienen los mismos servicios.

# Funciones claves router

- Ejecutar protocolos / algoritmos de routing (RIP (desuso), OSPF [más usado] ,  BGP)
- Reenviar datagramas del enlace de entrada al enlace de salida

Los enlaces de entrada y salida estan en el mismo disposivitovl, es la entrada de un paquete a un puerto y la salida a otro puerto

> Medir mbps: [Fast](https://fast.com/) , speedtest
CUando usamos estas paginas envian **un ping** y **esta utiiznaod el prtocolo ICMP** calculando la velocidad en enviar y en bajar.

**ICMP:** NO usa tcp ni UDP, es independiente que se **ejecuta en capa de transprote y red**

# Cola de puerto
SI tiene prorizacion con quality service, entre **video y arhcivo**, el video tiene trasnmision.

SI la velocidad de llegada es mayor a la velocidad de salida (por ejemplo llegan datos de entrada de fibra y la salida es de cobre, rapido a lento) y el procedador no alcanza a procesar la info hay retraso y perdidas de paquetes.

# REPETIDOR PARA AUMENTAR LA DISTANCIA DE SEÑAL

# Causas de retraso de paquetes

## Procesamiento en el nodo
EL paquete lega y el router se demora en procesarlo (chequeo de errores, desempaquetamiento)

## Colas
Ocurre cuanto entre y empieza a armarse colas pues es mas rapida la de enrada que salida. O en la salida pq la **propagacion**

**TRANSMITIR**: Poner el paquete ene l enlace, apsarlo del peurto de slaida al enlaxc e(ocurre un epmpaquemtamiento apra ponerlo en el enlace ). Se hace dentro del router
**PRPAGACION**: En enlace puede ser corto o largo, entonces la progrpagacion es el timepo que tarda de legar un paquete d eun nodo a otro, de un router a otro.

## Retardo (d) de trasnmisioin
Se da en el punto en donde el router (puerto) y el enlace se dan.

## Retardo de propagacion
Loa afecta al distnacia, la fisica del enlace y pues la velocidad de propagración.

# EL RETARDO EN UN ENLACE DE FIBRA SE DA EN EL PROCESADOR / ENRUTADOR

# Los paquetes descartados pueden ser retrasnmitidos por el nodo anterior o nodo origen (cuando no hay acuse de recibo con TCP) o no ser retransmitiro (se usa UDP)

# Para trasnmitir
LOs host tienen alamcenada al tabal de enrutamiento con las direccion que he consultado, con el comando `ǹetstat -r` muestra la tabla de enrutamiento.

# Si un router tiene que hacer traduccion de direcciones tiene que utilizar: Capa fisica, enlace, red

# LOs routers que utilzian la capa de trasnporte cuando tienen que hacer traduccion de direciones (Nat) `pues tienen que subir de capa.

