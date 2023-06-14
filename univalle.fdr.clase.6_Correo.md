---
id: 1tfq51j4gph04u1rm6kfi7c
title: 6_Correo
desc: ''
updated: 1685582884988
created: 1684969917525
---

Es el segundo mas usado en la capa de aplicacion

# Capa de aplicacion

## Enviar correo electronico

Necesito saber: Destinatario, nombre del servidor donde se enviara el correo electronico, 

EL SMPT se usa para conectarse a un servidor para enviar un correo

## Componentes del correo electronico

- Agente usuario o gestor de correo : Permite editar y crear un correo (usa SMTP pues su objetivo es enviar correos)
- Servidor de correo
- SImple MAil Transfer Protocol: SMTP Puerto 25 TCP

## Agente Usuario

- El **servicio para recibir** permite consultar una carpeta llaamada buzon o casilla de correo
- Los mensjaes enviados y recibidos son almacenados dentro del buzon en el servidor. Es decir que por cada usuario se almacena una cuenta ocupando un espacio.

# Servidor de correo contiene
- Casilla : Contiene mensajes de entrada para el usuario
- COla de mensajes: Correos en procesos de envio (outbox)
- SMTP: Protocolo entre servidores de correo para enviar msg emails

# SMTP

- Usa el TCP (protocolo de capa de transporte) para enviar mensajes de correo electronico.
Usa TCP pues debe asegurarse de que al otro lado del servidor hay un servicio de que valida que yo exista y que mi cuenta puede enviar correos.

> Lo primero que se necesita es un servicio funcionando y activo que este funcionando a traves de un puerto (25 es el puerto no seguro del SMTP) (587 o 485 creo para seguro telmet y ssh creo)

-Los comandos van en Texto ASCII

- Hay una conexion servidor a servidor: EL usuario envia el correo haciendo uso de un servicio activo a la esucha (se conecta al servicio verifcando que tenga cuent ay cuenta destinatario), el cual utiliza el protocolo SMTP para enviarlo y en esa interaccion se conecta a otro servidor que contiene la cuenta del destinatario y se envia el correo. EL servicio del segundo servidor debe ser un servicio POP3 O IMAP Pues se encarga de recibir (a diferencia del primero que se encarga de enviar) y entonces el serv1 pregunto al serv2 si esta activo y si tiene la cuenta del destinatario. El cliente debe conectarse (el cliente final)  para realizar una solictud, entonces el cliente2 quien llama al servidor2, se conecta y trae los correos.

DIferencia entre POP3 E IMAP
IMAP realiza una sincronizacion, es decir si borrar algo en el cliente se borra en el servidor y visceversa. Mientras que POP no realiza sincronizacion, es decir si borro algo en el cliente no se borra en el servidor y viceversa.

POP (puerto 110) y IMAP (puerto 143) son protocolos de capa de aplicacion que permiten a un usuario final recuperar correos electronicos desde un servidor de correo remoto.

> Los mensajes deben ser enviados en ASCII de 7 bits : Es decir que SMTP solo puede enviar mensajes de texto plano, no puede enviar imagenes, videos, etc.

## Envio de archivos multimedia : Extensiones multimedia

COmo smtp solo usa lo que dijimos en smtp hay que usar un protocolo el cual funciona como una extension al smtp para enviar multimedia. Este protocolo es el MIME (Multipurpose Internet Mail Extensions) el cual permite enviar archivos multimedia. Este protocolo permite enviar archivos binarios (no solo texto plano) y permite enviar archivos de cualquier tipo.

Se declaran lineas adicionales en el encabezado del mensaje que declara el tipo de contenido: 
- Versdion MIME
- Metodo de codificacion usado
- Tipo de datos multimedia
- Datos codificados

## Gestor de correo

SUrge en la necesidad de hacer uso del servicio SMTP como el del POP3 o IMAP. Es decir que surge la necesidad de hacer uso de un servicio que permita enviar y recibir correos electronicos.

## COmo se enviaban correos

Se debia conectar a telnet al servidor. Telnent funciona como app (conectarme a un servidor), como servicio (para dar respuesta) y como protocolo (hace conexiones TCP atravez de puertos y de más).

`telnet smtp.gmail.com 25` Si le damos 25 por defecto no se detecta pues ese puerto es inseguro y gmail no lo permite. Entonces se debe usar el puerto 587.

Comandos al hacer eso que puedes hacer : 
- HELO: Para saludar
- MAIL: Para especificar el remitente
- FROM: Para especificar el remitente
- RCPT TO: Para especificar el destinatario
- DATA : Para escribir el mensaje
- QUIT: Para salir

# Problemas comunes del protocolo SMTP

- SPAM: Mensajes o correos **no solicitados**. Marca como SPAM  aun sender no solicitado. 
- PHISHING: Mensajes que **solicitan informacion personal**. Es un tipo de SPAM.
- Malware: Mensajes que **contienen virus**. Es un tipo de SPAM.

# Protocolo POP3
Puerto por defecto: TCP 110

En telnet sería: `telnet pop.gmail.com 110`

Usamos el puerto 995 cuando queremos usar SSL (Secure Socket Layer) o TLS (Transport Layer Security) para cifrar la comunicacion. Asi: `telnet pop.gmail.com 995`

COmandos fase transaccional:
- list: Lista numero de los mensajes
- retr: extrae mensajes por su numero
- delete
- quit

Para enviar es 
telnet smtp.gmail.com 587
ehlo gmail.com
mail from: email
starttls
mail from: email
rcpt to: email
data
subject: asunto
mensaje

---

EL servidor de outlook (el smtp) es smtp.office365.com y el puerto es 587.

# DNS

Es un servicio de resolucion de nombres. Es decir que permite traducir nombres de dominio  (nombre host) a direcciones IP.

Es clave pues los dominios como gmail.com son aosicados entre nombre de dominio y una ip (algo necesario).

El servicio Domain Name System consiste en que el usaurio necesita acceder a una direccion IP. Entonces el usuario hace una peticion al DNS para que le de la IP de un dominio. El DNS le da la IP y el usuario se conecta a esa IP. 

Los dominios existen para poder recodarlos como usuarios, pues es mas facil que recordar una ip.

> Utiliza el protocolo de trasnporte UDP (User Datagram Protocol) en el puerto 53.


- Servidores DNS ROOT
  - com
    - yahoo
    - amazon
  - org
    - pbs.org
  - edu
    - poly.edu

Loos DNS Root NAME actuan como unca capa superior de todas en las que consulta para saber que esta en tal servidor.

REGISTRO TIPO **A** ASOCIADO DOMINIO CON IP (ASOCIA DIR<ECCION IP CON EL HOST)
REGISTRO TIPO **MX** ASOCIADO DOMINIO CON SERVIDOR DE CORREO
REGISTRO TIPO **CNAME** ASOCIADO DOMINIO CON OTRO DOMINIO (Diferentes nombres apuntado a la misma direccion IP)
REGISTRO TIPO **NS** LO ALMACENA UN SERVIDOR DNS PARA PODER REFERENCIAR A OTRO SERVIDOR DNS
REGISTRO TIPO **NS** ASOCIADO DOMINIO CON SERVIDOR DNS
REGISTRO TIPO **SOA** ES UN REGISTRO COMPLEMENTARIO QUE ALMACENA INFORMAICON ADICIONAL SOBRE EL DOMINIO Y SE ALMACENA EN EL MISMO SERVIDOR DNS, aunque no simpre es asi

## NIC
nic.co es el que adminsitra los dominios .co, los cuales se deben pagar y se registran por esta empresa.

## Consultas iterativas


## Consultas recursivas

PROXIMA CLASE CAPA DE TRASNPORTE
