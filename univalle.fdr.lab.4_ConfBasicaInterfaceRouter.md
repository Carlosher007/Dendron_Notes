---
id: 0swxl5ur56ith640fszguc6
title: 4_ConfBasicaInterfaceRouter
desc: ''
updated: 1680718136425
created: 1680712574955
---

# Tabla de direccionamiento

Con el numero X = 75
![](/assets/images/2023-04-05-11-37-31.png)

# Paso 1

- Configure las NIC de los PCs de acuerdo con la tabla de direccionamiento

> Una NIC es un hardware que permite aun dispositivo contectarse a una red, ya sea por cable o inalambricamente

En este paso debemos configurar la ip, mascara de red y puerta de enlace predeterminada en cada PC. Ademas de conectar a todos por sus respectivos cables.

Cuando conectemos **por medio de cable UTP** nos daremos cuenta de que los enlaces entre switchers y routers esta en rojo, pues las interfaces de los routers vienen deshabilitadas por defecto. Para habilitarlas debemos configurarlas.

## Tabla de direccionamiento de las NIC de los PCs

| PC | Interfaz | IP | MASCARA | GATEWAY |
| --- | --- | --- | --- | --- |
| PC1 | NIC | 192.168.75.10 | 255.255.255.0 | 192.168.75.1 |
| PC2 | NIC | 192.168.75.11 | 255.255.255.0 | 192.168.75.1 |
| PC3 | NIC | 192.168.76.10 | 255.255.255.0 | 192.168.76.1 |
| PC4 | NIC | 192.168.76.11 | 255.255.255.0 | 192.168.76.1 |

# Paso 2 : Configuracion del Router

Vamos al **CLI** del router y habilitamos el modo privilegiado con el comando `enable` y luego configuramos el router con el comando `conf t`

> Asigne el nombre R1
`hostname R1`


> Utilice su codigo como contraseña de EXEC del usuario para la consola 0
`line console 0`
`pass 2125653`
`login`

> Utilice su primer nombre como contraseña EXEC privilegiado
`enable secret carlos`

> Cifre todas las contraseñas
`service password-encryption`

> Configure el mensaje de bienvenida
`banner motd "Bienvenido al router R1"`

## Configuracion de acceso remoto por SSH

> Establezca el nombre de dominio en R1
> El nombre de dominio se usa en la configuración de SSH para identificar el nombre del host al que los usuarios se conectan.
`R1(config)# ip domain-name redes.com`

> Cree un usuario con una contraseña segura
`R1(config)# username Admin password Cisco123`

> Genere claves RSA de 1024 bits
> Las claves RSA se utilizan en el cifrado de datos en el protocolo SSH. Al generar claves RSA de 1024 bits, se está creando un par de claves pública y privada para el encriptado y desencriptado de los datos que se transmiten entre el cliente y el servidor en una conexión SSH.
`R1(config)# crypto key generate rsa`

> Bloquee durante tres minutos a cualquier persona que no pueda iniciar sesion despues de cuatros intentos en un periodo de dos minutos
`R1(config)# login block-for 180 attempts 4 within 120`

> Configure las lineas VTY para el acceso por SSH y solicite los perfiles de usuarios locales para la autenciacion
> Este paso configura las líneas VTY (Virtual Teletype) para permitir el acceso por SSH. También se solicita la autenticación de usuarios locales, lo que significa que los usuarios deben tener una cuenta en el router y una contraseña para iniciar sesión en el mismo. Esto ayuda a garantizar que solo los usuarios autorizados puedan acceder al router por SSH.
`R1(config)# line vty 0 4`
`R1(config-line)# transport input ssh`
`R1(config-line)# login local`

> Conectarse remotamente al R1 por SSH desde el command Prompt
`SSH -I Admin 192.168.75.1'

## Configure el direccionamiento IP para las interfaces del Router de acuerdo con la tabla de direccionamiento. 

En el CLI y en el modo privilegiado con el comando `enable` y luego configuramos el router con el comando `conf t` hacemos esto:

> Entro a la interzas
'int g 0/0'

> Configuro ip con la mascara de red
'ip add 192.168.75.1 255.255.255.0'

> Habilito la interfaz
'no shut'

> Vemos la tabla de enrutamiento
'show ip route'

Vemos que ahora la tabla de enrutamiento tiene una ruta por defecto hacia la red

> Hacemos lo mismo para la g 0/1  con ip 192.168.76.1

> Probamos la conexion por SSH desde el pc
`ssh -l Admin 192.168.75.1'

> Desde el CLI del router vemos el archivo de configuracion y lo guardamos en la NVRAM
`show run`
`copy run start`

## Configuracion de los Switch

> Configure el nombre del S1 y S2
En el CLI del Switch escribimos `hostname S1` o `hostname S2` estando en el modo privilegiado

> Configure el direccionamiento IP y el GW de acuerdo con la tabla de direccioamiento
> La configuración del direccionamiento IP y del gateway en un switch es importante para permitir la comunicación con otros dispositivos en la red. El direccionamiento IP se utiliza para identificar de manera única cada dispositivo en la red y permitir la comunicación entre ellos. El gateway predeterminado, o default gateway, se utiliza para enrutar el tráfico de red a través de la red hacia su destino.
> En el contexto del laboratorio, configurar el direccionamiento IP y el gateway en los switches según la tabla de direccionamiento asegurará que los switches estén en la misma subred que otros dispositivos de la red, lo que permitirá la comunicación entre ellos.

Para el S1:
`int vlan 1`
`ip address 192.168.75.254 255.255.255.0`
`ip default-gateway 192.168.75.1`

Para el S2:
`int vlan 1`
`ip address 192.168.76.254 255.255.255.0`
`ip default-gateway 192.168.76.1`


> Registre las interfaces con descripciones, incluida la interfaz VLAN 1 de los swtich

Para el S1:
`int vlan 1`
`desc VLAN 1`

Para el S2:
`int vlan 1`
`desc VLAN 1`