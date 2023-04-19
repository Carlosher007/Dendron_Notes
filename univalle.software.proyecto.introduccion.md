---
id: cfaf7evbhr1lzcc2vw3qojl
title: Introduccion
desc: ''
updated: 1681769024396
created: 1681181304713
---

# Aplicacion web: Concesionario de automoviles electricos

ORDEN DE TRABAJO: LLevar carro a arreglar, comprar repuestos, ver ordenes de trabajp

## Tareas

- Gestion de Inventario (Vehiculos y repuestos) de **cada sucursal**
- Cotizacion de vehiculos
- Venta de automoviles
- Reparaciones de vehiculos

## Usuarios

### Gerentes
Gestionar informacion relacionada a las sucursales, inventarios y crear roles 

### Vendedores
Gestionar cotizaciones y ventas de vehiculos

### Jefe de taller
Gestionar ordenes de trabajo o reparacion de vehiculos

### Clientes
Saber si mi vehiculo esta disponible o no, comprar y mas cositas

## Adicionales

- Cada proceso del sistema permite generar reportes en formato de texto y grafico
- Usar API  de visualizacion de google o alguna libreria en javascript para reportes
- Un proceso en modo transaccional
- Buscador para clientes
- Sistema en servidor que este en la nube
- Usar capcha, autenticacion usando el correo electronico, validacion de campos de form del lado de cliente y servidor
- Que datos son obligatorios para el registro de cada tipo de usuario
TANTO FISICO COMO DIGITAL LA  COMPRA


## Posible Maquetacion
### Pagina de inicio (TODOS LOS USUARIOS)

Sera un landing page que permita a los usuarios conocer los servicios y productos que ofrece el concesionaro. Se encontraran **botones de registro e inicio de sesion**. Tambien se incluira una seccion de detacados donde se mostraran los vehiculos ordenados por mas vendidos (Si no se ha vendido se muestra tal cual se traiga de la bd) y un formulario de busqueda para filtrar por vehiculo.

### Formulario de registro (TODOS LOS USUARIOS)

Crear a los usuarios una cuenta en el sistema. Una vez ingresen a este punto se les pedira **completar un captcha**. Luego se les desplegara la opcion para elegir el tipo de usuario y su respectivo formulario.

#### Gerente

Se le solicitara datos como nombre completo, correo electronico, contraseña, numero de telefono, sucursal a la que esta asignado

#### Vendedor

Se le solicitara datos como nombre completo, correo electronico, contraseña, numero de telefono, sucursal a la que esta asignado

#### Jefe de Taller

Se le solicitara nombre completo, correo electronico, contraseña, numero de telefono, sucursal a la que esta asignado

#### Cliente

Se le solicitara nombre completo, correo electronico, contraseña, numero de telefono, direccion identificacion (cedula, pasaporte, etc)

> Una vez se registre el usuario se le redigira a una pagina para confirmar su correo electronico y si lo confirma se le llevara al dashboard, de lo contrario tendrá que ir a la pagina de inicio. Si el usuario no confirma su correo electronico entonces su cuenta no quedara como activa y solamente podra ingresar a su dashboard cuando confirme el correo.

### Formulario de inicio de sesion

Se le solicitara al usuario su correo electronico y contraseña. Si el usuario olvido su contraseña se le enviara un correo electronico con un link para restablecerla.

### Dahsboard

Pagina principal para cada rol de usuario, donde se mostraran las funciones principales

### Pagina de perfil de usuario (TODOS LOS USUARIOS)

Pagina de perfil de usuario donde pueden ver y editar su informacion

### Pagina de administracion de usuarios (GERENTE)

Puede crear roles, así como tambien puede crear nuevos usuarios

### Pagina de sucursales (GERENTE)

Pueder ver y editar informacion de su sucursal

### Pagina de inventario de vehiculos (Gerente, Vendedor)

Se puede ver el inventario actual de vehiculos de cada sucursal disponibles en el consecionario. El gerente puede editar el inventario y los vendedores solo pueden verlo

### Pagina de inventario de respuestos (Gerente, Jefe de Taller)

Se puede ver el inventario actual de repuestos disponibles en el concesionario. El gerente puede editar el inventario y los vendedores solo pueden verlo.

### Pagina de compra (CLIENTE)

Se mostraran los vehiculos disponibles para la compra. El cliente podra filtrar por marca, modelo, precio, color, etc. Tambien podra ver el detalle de cada vehiculo y agregarlo a su carrito de compras.

### Pagina de cotizaciones (Gerente,Vendedor)

El vendedor Puede crear y enviar cotizaciones de los vehiculos. Entendiendo cotizaciones como el precio del vehiculo, así como diferentes opciones de compra (Con intereses y toda la vuelta). El gerente puede ver todas las cotizaciones

### Pagina de ventas de vehiculos realizados (Gerente, Vendedor)

Se pueden visualizar las ventas de vehiculos realizadas. El gerente puede ver todas las ventas y los vendedores solo pueden ver y gestionar sus propias ventas.

### Pagina de ordenes de trabajo (reparacion de vehiculos) (Gerente, Jefe taller)

Los jefes de taller pueden gestionar las ordenes de trabajo, es decir, las ordenes de reparacion de vehiculos.  Puede asignar mecanicos disponibles a cada tarea, actualizar el estado de las reparaciones y asignar fechas de entrega.

### Pagina de vehiculos (TODOS LOS USUARIOS)

Se mostraran todos los detalles de los vehiculos y de un vehiculo en especifico si así se desea, incluyendo descripcion, caracterisitcas, imagenes, precio. Los **clientes** podrán agregar el vehiculo a **su lista de favoritos** o cotizarlo.

### Lista de vehiculos favoritos (CLIENTES)

Pagina donde se muestran los vehiculos favoritos de los clientes. Puede visualizar toda la informaicon, cotizarlo o quitarlo de favoritos.

### Pagina de mis vehiculos (CLIENTES)

Podra ver los vehiculos adquiridos asi como tambien poder enviarlos a reparacion.

## Proceso de compra de un vehiculo

Una vez el cliente haya dado click en el vehiculo que desea comprar, el vendedor recibira una notificacion en su dashboard para que pueda gestionar la cotizacion y la venta.

El vendedor debera crear una cotiacion detallada para el cliente, que incluya el precio del vehiculo, opciones de financiamiento, tasas de interes, plazos de pago y otras cosas.

El cliente podrá elegir entre las opciones de pago y aceptar o rechazar la cotizacion.

Si el cliente acepta, el vendedor debera generar una factura y solicitar el pago. 

UNa vez el pago se haya completado, el cliente recibira una notificacion de que el vehiculo esta listo para ser entrgado y el vendedor puede gestionar la entrega del vehiculo al cliente.


## Historias de usuario



PRIMERA VERSION DEL PRODUCT BACKLOG