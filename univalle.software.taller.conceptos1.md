---
id: 60t36ch5xag8lfclhah8kuz
title: Conceptos1
desc: ''
updated: 1682519886056
created: 1682516198395
---

# Variables de Sesion

Son una forma de almacenar información temporalmente en el sevirdor, mientras un usuario interactua con la apliacion.

Cuando un usuario inicia sesion en una aplicacion web, se crea una sesion para esa persona. Durante esa sesion, la aplicacion web puede almacenar informacion especifica del usuario en variables de sesion. Esta infromacion se puede utilizar para personalizar la experiencia del usuario, mantener un estado de sesion y almacenar informacion que debe persistir a lo largo de mutliples solicitudes HTTP.

Las variables de sesión son específicas del usuario y no pueden ser accedidas por otros usuarios. Además, su información se elimina cuando el usuario finaliza la sesión o cuando la sesión expira.

## Variables de sesion: Algo del Backend

Las variables de sesión se manejan en el backend de una aplicación web y se utilizan para almacenar información temporal sobre la sesión del usuario mientras interactúa con la aplicación.

## Variables de sesion con Django y React

Para manejar variables de sesión en Django, puede utilizar la sesión de Django, que proporciona una interfaz para crear y administrar variables de sesión en el backend. Django manejará la gestión de sesiones en el servidor y proporcionará un identificador de sesión único que se utilizará para identificar al usuario en las solicitudes posteriores.

En el frontend, React puede interactuar con Django a través de una API RESTful para acceder a la información de sesión y realizar las operaciones necesarias en la aplicación. Por ejemplo, cuando un usuario inicia sesión, el frontend de React puede enviar una solicitud POST a la API de Django para autenticar al usuario y crear una sesión. Luego, el backend de Django generará un identificador de sesión único y devolverá esa información al frontend, que la almacenará en el estado global de la aplicación.

## Diferencia cookies y variables de sesion

Las cookies son pequeños archivos que se almacenan en el navegador del usuario y se utilizan para recordar información específica del usuario, como sus preferencias de idioma o su historial de navegación. Las cookies pueden ser creadas tanto en el lado del servidor como en el lado del cliente, y se pueden leer y modificar tanto en el lado del servidor como en el lado del cliente.

Por otro lado, las variables de sesión son variables que se almacenan en el servidor y se utilizan para mantener el estado de la sesión del usuario en el servidor. Cada sesión de usuario tiene una variable de sesión única, y esta variable se utiliza para almacenar información específica del usuario durante toda la sesión. Las variables de sesión se crean y se manejan únicamente en el lado del servidor y no pueden ser leídas o modificadas directamente por el cliente.

# Servidores Web

Un servidor web es un software que se encarga de servir páginas web a través de Internet. El servidor web recibe solicitudes HTTP de los clientes (navegadores web) y envía las páginas web correspondientes como respuesta. Los servidores web pueden servir páginas web estáticas (como archivos HTML, CSS o JavaScript) o páginas web dinámicas (generadas por un lenguaje de programación en el servidor).

## Nginex y Apache

- Arquitectura: Apache utiliza un modelo de procesamiento de hilos, mientras que Nginx utiliza un modelo de procesamiento de eventos, lo que permite manejar más conexiones concurrentes con menos recursos.

- Consumo de recursos: Nginx utiliza menos recursos que Apache para manejar el mismo número de conexiones, lo que lo hace más eficiente en términos de uso de recursos.

- Configuración: La configuración de Nginx es más simple y legible que la de Apache, lo que lo hace más fácil de configurar y mantener.

- Manejo de solicitudes: Nginx es más rápido que Apache en el manejo de solicitudes HTTP y HTTPS, lo que lo hace más adecuado para aplicaciones web de alta carga.

- Módulos: Apache tiene una gran cantidad de módulos disponibles para agregar funcionalidades a su servidor, mientras que Nginx tiene una cantidad más limitada de módulos disponibles.

- Popularidad: Apache es más popular que Nginx, especialmente en el mundo de los servidores web de código abierto, lo que significa que hay más documentación y soporte disponible para Apache.

# Get Y Post

GET y POST son dos métodos HTTP que se utilizan para enviar datos desde un cliente (como un navegador web) a un servidor.

La principal diferencia entre GET y POST es que GET se utiliza para solicitar datos del servidor y POST se utiliza para enviar datos al servidor.

En una solicitud GET, los datos se envían en la URL como parámetros de consulta. Por ejemplo, en la URL "http://ejemplo.com/buscar?query=python", "query=python" es un parámetro de consulta que se envía al servidor para realizar una búsqueda.

En una solicitud POST, los datos se envían en el cuerpo de la solicitud HTTP y no en la URL. Esto hace que los datos enviados por POST sean más seguros que los enviados por GET, ya que no se muestran en la URL y, por lo tanto, no se pueden interceptar fácilmente.