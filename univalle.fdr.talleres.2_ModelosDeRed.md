---
id: qax76d17qsbewm4gp0nmr7r
title: 2_ModelosDeRed
desc: ''
updated: 1681913951040
created: 1681587813931
---

# Diferencias entre los modelos OSI y TCP / IP

1. Número de capas: El modelo OSI consta de siete capas, mientras que el modelo TCP/IP consta de cuatro capas.

2. Enfoque: El modelo OSI se enfoca en la abstracción y la estandarización de la arquitectura de red, mientras que el modelo TCP/IP se enfoca en la funcionalidad y la implementación práctica.

3. Arquitectura: El modelo OSI es una arquitectura teórica que describe cómo debería funcionar una red de computadoras ideal, mientras que el modelo TCP/IP es una arquitectura práctica que se ha desarrollado a lo largo del tiempo en respuesta a las necesidades reales de las redes de computadoras.

4. Protocolos: El modelo OSI define protocolos para cada una de sus siete capas, mientras que el modelo TCP/IP utiliza una serie de protocolos para todas sus capas.

5. Flexibilidad: El modelo TCP/IP es más flexible que el modelo OSI, ya que permite que las capas se fusionen o se dividan según sea necesario para adaptarse a diferentes situaciones de red.

# Ventajas y desventajas (desde el punto de vista del desarrollador de aplicaciones) que presente la implementacion de OSI

- **Ventajas**
  - Estandarización: El modelo OSI proporciona un conjunto de estándares claros y bien definidos para la comunicación de red, lo que permite a los desarrolladores de aplicaciones diseñar y desarrollar aplicaciones que sean compatibles con cualquier red que utilice el modelo OSI.
  - Modularidad: El modelo OSI se divide en siete capas, lo que permite una mayor modularidad y separación de las responsabilidades. Esto hace que sea más fácil para los desarrolladores de aplicaciones comprender y depurar problemas de red, ya que cada capa se ocupa de una tarea específica.
  - Abstracción: El modelo OSI proporciona una capa de abstracción entre la aplicación y la red subyacente, lo que facilita el desarrollo de aplicaciones independientes de la plataforma que puedan comunicarse con diferentes redes.
- **Desventajas**
  - Complejidad: El modelo OSI es un modelo complejo que consta de siete capas, cada una con un conjunto de protocolos y estándares que deben ser comprendidos y seguidos por los desarrolladores de aplicaciones. Esto puede aumentar la complejidad del desarrollo y la dificultad de depurar problemas de red.
  - Implementación limitada: Aunque el modelo OSI es un estándar, su implementación en la práctica es limitada y no es ampliamente utilizado en la mayoría de las redes. Esto significa que los desarrolladores de aplicaciones pueden tener dificultades para encontrar redes que utilicen el modelo OSI y pueden necesitar aprender y adaptarse a diferentes modelos de red.
  - Poca flexibilidad: El modelo OSI no es tan flexible como otros modelos de red, como el modelo TCP/IP, y no se adapta fácilmente a diferentes situaciones de red. Esto puede dificultar la adaptación del modelo OSI a las necesidades específicas de una red en particular.

# Ventajas y desventajas (desde el punto de vista del desarrollador de aplicaciones) que presente la implementacion de TCP/IP

- **Ventajas**
  -     Implementación generalizada: El modelo TCP/IP es el modelo de red más ampliamente utilizado en la actualidad y se ha convertido en el estándar de facto para la mayoría de las redes de computadoras en todo el mundo. Esto significa que los desarrolladores de aplicaciones pueden contar con una amplia gama de herramientas y recursos disponibles para el desarrollo de aplicaciones que utilizan el modelo TCP/IP.

  - Flexibilidad: El modelo TCP/IP es más flexible que el modelo OSI, ya que permite que las capas se fusionen o se dividan según sea necesario para adaptarse a diferentes situaciones de red. Esto facilita la adaptación del modelo TCP/IP a las necesidades específicas de una red en particular.

  - Implementación más sencilla: El modelo TCP/IP es más simple que el modelo OSI y consta de sólo cuatro capas. Esto puede facilitar el desarrollo de aplicaciones y la depuración de problemas de red.
- **Desventajas**
  - Falta de estandarización: A diferencia del modelo OSI, el modelo TCP/IP no proporciona un conjunto de estándares claros y bien definidos para la comunicación de red. Esto puede dificultar la compatibilidad entre diferentes redes y puede requerir una mayor inversión de tiempo y recursos para la depuración de problemas de red.

  - Falta de modularidad: El modelo TCP/IP no se divide en capas tan claramente definidas como el modelo OSI, lo que puede dificultar la comprensión y la depuración de problemas de red.

  - Menor abstracción: El modelo TCP/IP proporciona menos abstracción entre la aplicación y la red subyacente que el modelo OSI. Esto significa que los desarrolladores de aplicaciones pueden necesitar entender más sobre la red subyacente para implementar su aplicación.

# Cual es el proposito del nivel de enlace

El nivel de enlace, también conocido como capa de enlace de datos, es la capa número dos del modelo OSI y del modelo TCP/IP. El propósito principal del nivel de enlace es proporcionar un medio para transferir datos de forma fiable entre dos dispositivos directamente conectados en la misma red física.

El nivel de enlace se ocupa de la transmisión de datos en paquetes de red, conocidos como tramas, desde un dispositivo de origen a un dispositivo de destino.La capa de enlace de datos se encarga de coordinar el acceso al medio de transmisión, la detección y corrección de errores, y el control de flujo para garantizar una comunicación eficiente y sin errores entre los dispositivos de la red.

# Que servicios provee el nivel de trasnporte? En que tipo de aplicaciones seria preferible TCP? Y en que tipo de aplicaciones seria preferible UDP?

El nivel de transporte es la cuarta capa del modelo OSI y del modelo TCP/IP, y tiene como objetivo proporcionar servicios de comunicación extremo a extremo para las aplicaciones que se ejecutan en diferentes dispositivos finales.

Los servicios principales que proporciona el nivel de transporte son:

- Multiplexación de conexión: el nivel de transporte permite que varias aplicaciones se comuniquen simultáneamente utilizando una única conexión de red. Esto se logra mediante la identificación de las aplicaciones utilizando números de puerto únicos.

- Segmentación y reensamblaje de datos: el nivel de transporte divide los datos en segmentos más pequeños para su transmisión a través de la red, y luego los reensambla en el extremo receptor para formar los datos originales. Esto permite que se transmitan grandes cantidades de datos de manera eficiente y fiable a través de redes de baja calidad.

- Control de flujo: el nivel de transporte regula el flujo de datos para garantizar que un dispositivo receptor no se sature con datos que no puede procesar. Esto se logra mediante el uso de técnicas como la ventana deslizante.

---

TCP (Transmission Control Protocol) es un protocolo orientado a la conexión que proporciona un servicio de comunicación confiable y ordenado. Esto significa que TCP establece una conexión entre dos dispositivos finales y luego garantiza que todos los datos enviados a través de esa conexión se entreguen de manera confiable y en el orden correcto

UDP (User Datagram Protocol) es un protocolo sin conexión que proporciona un servicio de comunicación no confiable y no ordenado. Esto significa que UDP simplemente envía los paquetes de datos a través de la red sin garantizar que lleguen a su destino o en qué orden se entregan. UDP se utiliza comúnmente en aplicaciones que requieren una transmisión de datos rápida, como videojuegos, transmisiones de video en tiempo real y voz sobre IP (VoIP).

---

En cuanto a las aplicaciones, es preferible utilizar el protocolo TCP en aplicaciones que requieren una transmisión de datos fiable y ordenada, como transferencias de archivos, correos electrónicos, navegación web, transacciones bancarias en línea, entre otras. TCP garantiza que todos los paquetes lleguen a su destino, y si un paquete se pierde o llega dañado, TCP lo retransmite hasta que se confirma su recepción correctamente. Sin embargo, este proceso de retransmisión y garantía de entrega puede hacer que la transmisión de datos sea un poco más lenta.

Por otro lado, el protocolo UDP es preferible en aplicaciones que no requieren una transmisión de datos fiable y que pueden tolerar la pérdida ocasional de paquetes. Ejemplos de este tipo de aplicaciones son la transmisión en tiempo real de audio y video, juegos en línea, servicios de voz sobre IP, entre otros. UDP es más rápido que TCP, ya que no tiene que esperar confirmaciones de recepción, pero la ausencia de garantía de entrega puede resultar en paquetes perdidos o entregados fuera de orden. 

# Que servicios provee el nivel de sesion? Cual seria su proposito en el desarrollo de una aplicaciones cliente /servidor?

El nivel de sesión es una capa del modelo OSI que proporciona servicios para establecer, mantener y finalizar las sesiones entre dos dispositivos finales. El propósito principal del nivel de sesión es permitir que las aplicaciones en diferentes dispositivos finales establezcan una sesión de comunicación y realicen intercambios de datos.

El nivel de sesión proporciona varios servicios a las aplicaciones, como el control de diálogo (para coordinar la comunicación entre las aplicaciones), la gestión de tokens (para evitar la colisión de datos entre las aplicaciones) y el control de sincronización (para permitir que las aplicaciones en diferentes dispositivos finales mantengan una vista coherente de los datos).

En el desarrollo de una aplicación cliente/servidor, el nivel de sesión juega un papel importante en la coordinación de la comunicación entre los clientes y el servidor. Por ejemplo, cuando un cliente desea establecer una sesión con un servidor, la capa de sesión se encarga de establecer y mantener la sesión durante la comunicación. También se encarga de manejar errores y situaciones inesperadas, como la interrupción de la conexión entre el cliente y el servidor.

# Que funciones provee ele nivel de presentacion? Cual seria su proposito en una aplicacion cliente/servidor?

El nivel de presentación es una capa del modelo OSI que se encarga de la presentación de datos para su transmisión a través de la red. El propósito principal del nivel de presentación es proporcionar servicios que permitan a las aplicaciones en diferentes dispositivos finales intercambiar información en un formato común, independiente del sistema operativo, la plataforma o la codificación utilizada.

El nivel de presentación proporciona varias funciones, como la conversión de la representación de datos de una aplicación a otra, la compresión y descompresión de datos para minimizar la cantidad de datos transmitidos a través de la red, la encriptación y desencriptación de datos para garantizar la seguridad y la integridad de los datos, y la gestión de la sintaxis y semántica de los datos intercambiados.

En una aplicación cliente/servidor, el nivel de presentación es importante porque ayuda a garantizar que la información se intercambie de manera efectiva entre el cliente y el servidor. Por ejemplo, si un cliente envía datos en un formato específico y el servidor utiliza un formato diferente, el nivel de presentación puede convertir los datos en un formato común para garantizar que el servidor los pueda procesar correctamente. También puede proporcionar funciones de seguridad, como la encriptación de datos confidenciales para protegerlos durante la transmisión.
