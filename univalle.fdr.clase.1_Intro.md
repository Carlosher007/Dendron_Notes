---
id: lwd593uy9uh3yofc1sx5jo4
title: 1_Intro
desc: ''
updated: 1681583883052
created: 1681568178840
---

# Actividad Exploratoria

## Que es una red de computadores

Conjunto de diospositivos electronicos interconectados entre si para compartir recursos e informacion, permitiendo enviar y recibir datsos.

## Para que se usan las redes

Para permitir la comunicacion entre dispositivos electronicos, para compartir recursos e informacion, para enviar y recibir datos. Por ejemplo el acceso al internet.

## Como podemos clasificar las redes

Se pueden clasificar de las siguientes maneras:

### Segun su alcance

> Red de area personal (PAN): Es una red que conecta dispositivos electronicos en un area de trabajo personal, como por ejemplo un ordenador y un telefono movil. EL bluetooth es un ejemplo de tecnologia PAN.
> Red de area local (LAN): Es una red que conecta dispositivos electronicos en un area local, como por ejemplo una oficina o un edificio. 
> Red de area metropolitana (MAN): Es una red que conecta dispositivos electronicos en una area metropolitana, como por ejemplo una ciudad.
> Red de are amplia (WAN): Es una red que conecta dispositivos electronicos en una area amplia, como por ejemplo un pais.

### Segun su tecnologia de conexion

> Red de cable: Es una red que conecta dispositivos electronicos mediante cables.
> Red inalambrica: Es una red que conecta dispositivos electronicos mediante ondas electromagneticas.

### Segun su tipologia de red

> De estrella: Todos los dispitivos se conectan a un nodo central, como por ejemplo un router.
> Topologia de bus: Todos los dispositivos se conectan a un cable central (en una linea unica), como por ejemplo un cable coaxial.
> Topologia de anillo: Los dispositivos se conectan en un circuito cerrado
> Topologia de malla: Todos los dispositivos se conectan entre si

## Que es la direccion MAC y para que sirve

La direccion MAC se utiliza en lugar de la direccion IP cuando se trata de la comunicacion entre dispositivos en la misma red local,

Se utiliza en lugar de la direccion IP cuando se trata de la comunicacion entre dispositivos en la misma red local,

# Red de comunicacion

## Dispositivos terminales

Son aquellos dispositivos que pueden enviar o recibir datos ( o ambos)  y son la fuente o el destino final de la informacion que se transmite a traves de la red. Por ejemplo un PC.

## Comutacion de paquetes en la red

Son los dispositovs que se encargan de que los paquetes de datos se transmitan de un dispositivo a otro. Por ejemplo un router,

# Equipos de conexion

## Conmutador (Hub, Switch, Router)

Se utiliza para conectar varios dispositivos en una red de comunicacion

La principal diferencia entre un hub, un switch y un router es la forma en que manejan y dirigen el tráfico de datos en la red. Un hub simplemente transmite los datos que recibe a todos los dispositivos conectados a él, lo que significa que todos los dispositivos reciben los mismos datos al mismo tiempo, independientemente de si esos datos son relevantes para ellos o no. Debido a esto, los hubs son menos eficientes que los switches en términos de ancho de banda y seguridad.

Los routers son dispositivos que se utilizan para interconectar diferentes redes y permitir que los dispositivos de una red se comuniquen con dispositivos en otra red. Los routers utilizan la dirección IP de los dispositivos para enrutar los paquetes de datos a través de la red. Los routers toman decisiones sobre la ruta que deben seguir los paquetes de datos para llegar a su destino final.

Los switches, por otro lado, se utilizan para conectar dispositivos dentro de una misma red. Los switches utilizan la dirección MAC de los dispositivos para enrutar los paquetes de datos a través de la red. Los switches son capaces de determinar qué dispositivos están conectados a cada uno de sus puertos y, por lo tanto, saben cómo dirigir los paquetes de datos a su destino final.

# Protocolo

Conjunto de reglas usadas por computadoras para comunicarse a traves de una red.

| Protocolo | Descripcion                                                                                                                                                                                                                           |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TCP/IP    | Especifica los mecanismos de formateo, direccionamiento y enrutamiento que garantia que los mensajes se entrguen al destino correcto. Es el protocolo principal utilizado en la mayoría de las redes de área amplia (WAN) e Internet. |
| HTTP      | Protocolo de transferencia de hipertexto. Utilizado para transferir datos de la World Wide Web (WWW).                                                                                                                                 |
| FTP       | Protocolo de transferencia de archivos. Utilizado para transferir archivos entre dispositivos en una red                                                                                                                              |
| SMTP      | Protocolo simple de transferencia de correo. Utilizado para el envío de correo electrónico.                                                                                                                                           |
| SSH       | Protocolo seguro de shell. Utilizado para acceder de forma remota a dispositivos de manera segura.                                                                                                                                    |


# Capas

1. Fisica
2. Enlace de datos
3. Red
4. Transporte
5. Sesion
6. Presentacion
7. Aplicacion

## Capa de aplicacion

Es la capa mas alta de la arquitectura de red. Es la capa que se comunica directamente con el usuario. Por ejemplo el protocolo HTTP.

Residen las aplicaciones de red y sus protocoles. Al paquete de infromacion se le llama **mensaje**

## Capa de transporte

Es la capa que se encarga de la comunicacion entre dos dispositivos. Por ejemplo el protocolo TCP (servicio orientado a la conexion) y UDP (servicio no orientado a la conexion).

Trasnporta los mensajes de la capa de aplicacion entre dispositvios finales. Al parque de informacion se llama **segmento**

### Ventajas de un protocolo orientado a conexion

Un protocolo orientado a conexión es aquel que establece una conexión entre dos dispositivos antes de iniciar la transmisión de datos.

Significa que dos dispositivos que desean comunicarse se envían señales de control para verificar que están disponibles y que pueden comunicarse. Una vez que se establece la conexión, los dispositivos pueden transmitir los datos de manera más eficiente y segura, ya que se han establecido parámetros de control de flujo, control de congestión y garantía de entrega de datos

### Ventajas de un protocolo no orientado a conexion

Los protocolos no orientados a conexión son más eficientes, escalables, flexibles y tienen una menor sobrecarga de señales de control en la red, lo que los hace ideales para redes grandes y complejas con un alto volumen de tráfico de datos.

## Capa de red

Es la capa que se encarga de la comunicacion entre dos dispositivos en redes diferentes. 

Se encarga de enrutar los paquetes de la capa de transporte de un dispositivo a otro a traves de una red de enrutadores.

La capa de trasnporte entrega a la capa de red **un segmento**, una **direccion de destino** y **un puerto**. Al paquete de informacion se le llama **datagrama**

### Protocolo IP

Protocolo de esta capa que define la forma en como los enrutadores y dispositivos finales interactuan con los datagramas.

## Capa de enlace 

Es la capa que se encarga de la comunicacion entre dos dispositivos en una misma red.

Al paquete de informacion se le llama **trama**

Algunos protocolos son: Ethernet, Token Ring, FDDI, etc.

### Capa fisica

Se encarga de mover **bits** individuales que conforman una trama, de un nodo a otro en la red.

Se encarga de la transmisión física de los datos a través de un medio de transmisión, como cables de cobre, fibra óptica o ondas de radio. La capa física define las características eléctricas, mecánicas y funcionales del medio de transmisión, como la velocidad de transmisión, la frecuencia, la modulación y la topología de la red

