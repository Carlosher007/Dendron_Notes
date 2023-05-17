---
id: nsl3ggqwwt9oqjlesg5rov7
title: Conceptos
desc: ''
updated: 1683670489266
created: 1682113822710
---

# <a id='Internet'>Internet</a>

Internet es una red de redes que permite la comunicación y el intercambio de información entre dispositivos conectados en todo el mundo. Siendo una red global de computadoras interconectadas que utilizan un conjunto de protocolos de comunicacion comunes para compartir información.

# <a id='ISP'>ISP</a>

Signficia Internet Service Provider. Es una empresa que proprociona servicios de acceso a Internet a particulares y empresas. Los ISP proporcionan conexiones a INternet con diversidad de tecnologias, como línea telefonica, fibra optica, conexión por cable o satelital.

# <a id='PAN'>PAN</a>

Red de area personal

Es una red que conecta dispositivos electronicos en un area de trabajo personal, como por ejemplo un ordenador y un telefono movil. EL bluetooth es un ejemplo de tecnologia PAN.

# <a id='LAN'>LAN</a>

Red de area local

Es una red que conecta dispositivos electronicos en un area local, como por ejemplo una oficina o un edificio. 

# <a id='MAN'>MAN</a>

Red de area metropolitana

Es una red que conecta dispositivos electronicos en una area metropolitana, como por ejemplo una ciudad.

# <a id='WAN'>WAN</a>

Red de area amplia

Es una red que conecta dispositivos electronicos en una area amplia, como por ejemplo un pais.

# <a id='Red-de-cable'>Red de cable</a>

Redes que utilizan medios de trasmision fisico como cables de cobre, fibra optica o coaxial para transmitir datos entre dispositivos. Alguno de los tipos mas comunes son [Redes-ethernet](./univalle.fdr.conceptos.md#Redes-ethernet), [Redes-de-fibra-optica](./univalle.fdr.conceptos.md#Redes-de-fibra-optica) y [Redes-de-cable-coaxial](./univalle.fdr.conceptos.md#Redes-de-cable-coaxial)

# <a id='Red-inalambrica'>Red-inalambrica</a>

Una red que utiliza ondas de radio para transmitir datos entre dispositivos. COmunmente conocidas como WLAN y son populares debido a su facilidad de instalacion y flexibilidad de eso.  Los tipos mas comunes son **WIFI, Bluetooth y redes satelitales**

# <a id='Redes-ethernet'>Redes-ethernet</a>

Son redes [LAN](./univalle.fdr.conceptos.md#LAN) que utilizan cables de cobre, generalmente [UTP](./univalle.fdr.conceptos.md#UTP) o [STP](./univalle.fdr.conceptos.md#STP), para transmitir datos a través de un medio físico.

# <a id='Redes-de-fibra-optica'>Redes-de-fibra-optica</a>

Utilizan cables de fibra optica para transmitir datos, los cuales consisten en hebras de vidrio delgadas y flexibles, capces de trasnportar datos a altas velocidades mediante la transmision de pulsos de luz.

Tiene ventajas como velocidad, mayor capacidad de trasnmision, menor atenuacion de la señal (viajar mas largo sin perder calidad). Pero es mas costoso.

# <a id='Redes-de-cable-coaxial'>Redes-de-cable-coaxial</a>

Utilizan un tipo de cable que consiste en un nucle de cobre o aluminio rodeado por un material aislante, una malla de cobre o aluminio. Se utilizan apra transmitir señales de audio, video y datos.

En cuanto a los usos, las redes de cable coaxial se utilizan principalmente en servicios de televisión por cable y en algunas redes de Internet.

# <a id='UTP'>UTP</a>

Es un tipo de cable de cobre utilizado en las [Redes-ethernet](./univalle.fdr.conceptos.md#Redes-ethernet). Tambien denominado cable de par trenzado sin blindaje, es un tipo de cable que utiliza dos hilos de cobre entrelazados para transmitir señales de datos. El UTP es el tipo de cable más comúnmente utilizado debido a su bajo costo, flexibilidad y facilidad de instalación.

# <a id='STP'>STP</a>

Es un tipo de cable de cobre utilizado en las [Redes-ethernet](./univalle.fdr.conceptos.md#Redes-ethernet). Tambien llamado par trenzado blindado, es un tipo de cable que utiliza una capa de metal (generalmente cobre) para proteger los hilos de cobres interntos, actuando como blindaje contra interferencias electromagneticas. Ofrece una mejor protección contra las interferencias electromagnéticas, pero es más costoso y más difícil de instalar que e

# <a id='Topologia-de-estrella'>Topologia-de-estrella</a>

En una topología de estrella, cada dispositivo de la red se conecta directamente a un nodo central (como un switch o un hub) utilizando un cable separado. Todos los datos que se transmiten entre los dispositivos de la red deben pasar por el nodo central. Esta topología es fácil de configurar y mantener, ya que es posible agregar o quitar dispositivos de la red sin interrumpir el resto de la red. Sin embargo, si el nodo central falla, toda la red se detiene.

# <a id='Topologia-de-bus'>Topologia-de-bus</a>

En una topología de bus, cada dispositivo de la red se conecta a un cable común (llamado bus) que se extiende a través de toda la red. Los datos que se transmiten entre los dispositivos de la red se envían a través del cable de bus. Esta topología es económica y fácil de instalar, ya que se requiere menos cableado que en una topología de estrella. Sin embargo, si un dispositivo de la red falla, puede interrumpir el flujo de datos en toda la red.

# <a id='Topologia-de-anillo'>Topologia-de-anillo</a>

En una topología en anillo, los dispositivos de la red se conectan en un anillo cerrado, en el cual cada dispositivo se conecta a los dispositivos vecinos. La señal de datos se mueve en una dirección en el anillo, y cada dispositivo actúa como repetidor para amplificar la señal antes de pasarla al siguiente dispositivo. Esta topología es resistente a fallas, ya que si un dispositivo falla, la señal puede seguir pasando por el anillo en la otra dirección. Sin embargo, si el anillo se interrumpe, toda la red se detiene.

# <a id='Topologia-de-malla'>Topologia-de-malla</a>

En una topología en malla, cada dispositivo se conecta directamente a cada uno de los otros dispositivos de la red. Esto permite múltiples rutas de comunicación entre los dispositivos, lo que hace que esta topología sea muy resistente a fallas y garantiza una alta disponibilidad de la red. Sin embargo, la topología en malla puede ser costosa de implementar, ya que requiere una gran cantidad de cableado y dispositivos de red.

# <a id='MAC'>MAC</a>

Media Acces Control es un **identificador unico** asignado a la interfaz de red (NIC) de un dispositivo. Es una serie de 12 digitos hexadecimales utilziados para **identificar de manera unica un dispositivo en la red**

Se utiliza en la [Capa-de-enlace-de-datos-OSI](./univalle.fdr.conceptos.md#Capa-de-datos-OSI) para proporcionar una identificacion unica de la NIC de un dispositivo de red. 

Tambien es así en el modelo TCP/IP y se usa para **la transmision de paquetes de datos entre dispositivos dentro una misma red local LAN**

La dirección MAC se utiliza para asegurar que los datos sean enviados al dispositivo correcto dentro de la misma red.  

# <a id='IP'>IP</a>

La dirección IP es un identificador único asignado a un dispositivo en una red y se utiliza para direccionar los paquetes de datos a su destino.

Se utiliza en la [Capa-de-red-OSI](./univalle.fdr.conceptos.md#Capa-de-datos-OSI)  y se utiliza para enrutar los datos a través de diferentes redes. Cada dispositivo en una red tiene una dirección IP única que se utiliza para identificarlo en la red y para enrutar los datos a su destino a través de la red.

Se utiliza para la comunicación en distintas redes.

# <a id='Dispositivos-terminales'>Dispositivos-terminales</a>

Los dispositivos terminales son aquellos dispositivos finales en una red que actúan como puntos de origen o destino de los datos. Estos dispositivos suelen ser computadoras, dispositivos móviles, servidores, impresoras y otros dispositivos de red que requieren acceso a la red para enviar o recibir datos.

# <a id='Conmutacion-de-paquetes'>Conmutacion-de-paquetes</a>

La conmutación de paquetes es una técnica utilizada en redes de computadoras para transmitir datos de un nodo a otro de manera eficiente y confiable. En esta técnica, los datos se dividen en paquetes más pequeños, que se transmiten a través de la red de manera independiente y se reensamblan en el destino.

# <a id='Hub'>Hub</a>

Utilizado para conectar varios dispositivos en una red : Un hub simplemente transmite los datos que recibe a todos los dispositivos conectados a él, lo que significa que todos los dispositivos reciben los mismos datos al mismo tiempo, independientemente de si esos datos son relevantes para ellos o no. Debido a esto, los hubs son menos eficientes que los switches en términos de ancho de banda y seguridad.

# <a id='Switch'>Switch</a>

Se utilizan para conectar dispositivos dentro de una misma red. Los switches utilizan la dirección MAC de los dispositivos para enrutar los paquetes de datos a través de la red. Los switches son capaces de determinar qué dispositivos están conectados a cada uno de sus puertos y, por lo tanto, saben cómo dirigir los paquetes de datos a su destino final.

# <a id='Router'>Router</a>

Los routers son dispositivos que se utilizan para interconectar diferentes redes y permitir que los dispositivos de una red se comuniquen con dispositivos en otra red. Los routers utilizan la dirección IP de los dispositivos para enrutar los paquetes de datos a través de la red. Los routers toman decisiones sobre la ruta que deben seguir los paquetes de datos para llegar a su destino final.

# <a id='Protocolo'>Protocolo</a>

Un protocolo se refiere a un conjunto de reglas y estándares que se utilizan para permitir que los dispositivos de una red se comuniquen entre sí y para garantizar que la comunicación sea confiable y segura.

# <a id='TCP/IP'>TCP/IP</a>

TCP/IP es un conjunto de reglas y protocolos que se utilizan para que los dispositivos de una red se comuniquen entre sí de manera confiable y eficiente. Se utiliza en Internet y en la mayoría de las redes informáticas para transferir datos, como correos electrónicos, archivos y páginas web.

Sus capas son:

1. [Capa-de-aplicacion-TCP/IP](./univalle.fdr.conceptos.md#Capa-de-aplicacion-TCP/IP)
2. [Capa-de-transporte-TCP/IP](./univalle.fdr.conceptos.md#Capa-de-transporte-TCP/IP)
3. [Capa-de-internet-TCP/IP](./univalle.fdr.conceptos.md#Capa-de-internet-TCP/IP)
4. [Capa-de-acceso-a-la-red-TCP/IP](./univalle.fdr.conceptos.md#Capa-de-acceso-a-la-red-TCP/IP)

# <a id='Capa-de-aplicacion-TCP/IP'>Capa-de-aplicacion-TCP/IP</a>

Esta capa es la capa más alta del modelo TCP/IP y es responsable de proporcionar servicios de red a las aplicaciones de usuario, como el correo electrónico, la navegación web y la transferencia de archivos.

# <a id='Capa-de-transporte-TCP/IP'>Capa-de-transporte-TCP/IP</a>

Esta capa es responsable de proporcionar un canal de comunicación fiable entre dispositivos de red. Los protocolos de esta capa, como TCP (Transmission Control Protocol) y UDP (User Datagram Protocol), se utilizan para establecer y mantener conexiones de red y garantizar la entrega de paquetes de datos.

# <a id='Capa-de-internet-TCP/IP'>Capa-de-internet-TCP/IP</a>

Esta capa es responsable de enrutar los paquetes de datos a través de una red. El protocolo principal de esta capa es el Protocolo de Internet (IP), que se encarga de la entrega de paquetes a través de la red y de identificar dispositivos en la red.

# <a id='Capa-de-acceso-a-la-red-TCP/IP'>Capa-de-acceso-a-la-red-TCP/IP</a>

Esta capa es la capa más baja del modelo TCP/IP y es responsable de la transmisión física de datos a través de la red. Esta capa define los medios y tecnologías utilizados para conectar dispositivos de red, como Ethernet, Wi-Fi y DSL.

# <a id='OSI'>OSI</a>

Es un modelo de referencia utilizado en redes de computadoras para estandarizar la comunicación entre dispositivos de diferentes fabricantes. El modelo OSI divide el proceso de comunicación en redes en siete capas lógicas, cada una con una función específica.

1. [Capa-Fisica-OSI](./univalle.fdr.conceptos.md#Capa-Fisica-OSI)

2. [Capa-de-enlace-de-datos-OSI](./univalle.fdr.conceptos.md#Capa-de-enlace-de-datos-OSI)

3. [Capa-de-red-OSI](./univalle.fdr.conceptos.md#Capa-de-red-OSI)

4. [Capa-de-transporte-OSI](./univalle.fdr.conceptos.md#Capa-de-transporte-OSI)

5. [Capa-de-sesion-OSI](./univalle.fdr.conceptos.md#Capa-de-sesion-OSI)

6. [Capa-de-presentacion-OSI](./univalle.fdr.conceptos.md#Capa-de-presentacion-OSI)

7. [Capa-de-aplicacion-OSI](./univalle.fdr.conceptos.md#Capa-de-aplicacion-OSI)

# <a id='Capa-fisica-OSI'>Capa-fisica-OSI</a>

Esta capa se encarga de la transmisión de datos a través del medio físico, como cables o aire, y establece las especificaciones técnicas para la transmisión de señales.

Se encarga de mover **bits** individuales que conforman una trama, de un nodo a otro en la red.

# <a id='Capa-de-enlace-de-datos-OSI'>Capa-de-enlace-de-datos-OSI</a>

Esta capa se encarga de la transmisión de datos entre dispositivos de una misma red y detecta y corrige errores de transmisión.

Al paquete de informacion se le llama **trama**

Algunos protocolos son: Ethernet, Token Ring, FDDI, etc.

# <a id='Capa-de-red-OSI'>Capa-de-red-OSI</a>

Es la capa que se encarga de la comunicacion entre dos dispositivos en redes diferentes, asegurandose que llegue a su destino. 

Al paquete de informacion se le llama **paquete**

# <a id='Capa-de-trasnporte-OSI'>Capa-de-trasnporte-OSI</a>

Trasnporta los mensajes de la capa de aplicacion entre dispositvios finales.

Al paquete de informacion se llama **segmento**

Esta capa se encarga de la gestión de los datos y de su entrega de manera confiable y ordenada.

# <a id='Capa-de-sesion-OSI'>Capa-de-sesion-OSI</a>

Esta capa se encarga de establecer, mantener y finalizar las sesiones entre dos dispositivos.

Al paquete de informacion se le llama **datagrama**

# <a id='Capa-de-presentacion-OSI'>Capa-de-presentacion-OSI</a>

Esta capa se encarga de la presentación de los datos y de su conversión a un formato que pueda ser entendido por el receptor.

# <a id='Capa-de-aplicacion-OSI'>Capa-de-aplicacion-OSI</a>

Esta capa se encarga de la comunicación entre las aplicaciones y la red, y proporciona servicios de red a las aplicaciones. Se comunica directamente con el usuario. Por ejemplo el protocolo HTTP.

Residen las aplicaciones de red y sus protocoles. Al paquete de infromacion se le llama **mensaje**

# <a id='HTTP'>HTTP</a>

Protocolo de transferencia de hipertexto. Utilizado para transferir datos de la World Wide Web (WWW).

# <a id='FTP'>FTP</a>

Protocolo de transferencia de archivos. Utilizado para transferir archivos entre dispositivos en una red.

# <a id='SMTP'>SMTP</a>

Protocolo simple de transferencia de correo. Utilizado para el envío de correo electrónico.  

# <a id='SSH'>SSH</a>

Protocolo seguro de shell. Utilizado para acceder de forma remota a dispositivos de manera segura.

# <a id='Protoco-orientado-a-conexion'>Protoco-orientado-a-conexion</a>

Un protocolo orientado a conexión es aquel que establece una conexión entre dos dispositivos antes de iniciar la transmisión de datos.

Significa que dos dispositivos que desean comunicarse se envían señales de control para verificar que están disponibles y que pueden comunicarse. Una vez que se establece la conexión, los dispositivos pueden transmitir los datos de manera más eficiente y segura, ya que se han establecido parámetros de control de flujo, control de congestión y garantía de entrega de datos

# <a id='Protocolo-no-orientado-a-conexion'>Protocolo-no-orientado-a-conexion</a>

Un protocolo no orientado a conexión es un protocolo de comunicación en el que los dispositivos no establecen una conexión previa antes de enviar datos. En otras palabras, los datos se envían sin verificar si el dispositivo receptor está disponible o no.

La principal ventaja de los protocolos no orientados a conexión es que son más rápidos y eficientes que los [Protocolo-orientado-a-conexion](./univalle.fdr.conceptos.md#Protoco-orientado-a-conexion), ya que no se requiere un proceso de establecimiento de conexión previo. Esto significa que pueden manejar grandes cantidades de datos en un corto período de tiempo y son ideales para aplicaciones en tiempo real, como la transmisión de video y audio.

Sin embargo, debido a la falta de verificación de conexión, los protocolos no orientados a conexión pueden ser menos confiables que los protocolos orientados a conexión, ya que los datos pueden perderse o entregarse en un orden diferente al que fueron enviados. Por lo tanto, deben utilizarse en situaciones donde la velocidad es más importante que la confiabilidad, y donde la pérdida ocasional de datos no es crítica.

# <a id='PDU'>PDU</a>

Protocol Data Unit es un término utilizado para describir los diferentes bloques de información que se intercambian entre dispositivos en una red de comunicaciones.

# <a id='RTT'>RTT</a>

Ruunt Trip time: Tiempo ocupado en enviar un paquete pequeño desde el cliente al servidor y su regleso