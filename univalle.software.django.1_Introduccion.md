---
id: fa819yano5xsplwsnygtrb7
title: 1_Introduccion
desc: ''
updated: 1680043685610
created: 1680043669959
---
# Django

## Instalar Django en Arch

Instale Python y pip con el siguiente comando:

```bash
sudo pacman -S python python-pip
```

A continuación, instale el entorno virtual de Python, que le permitirá crear un entorno aislado de Python para instalar Django sin afectar a otros paquetes del sistema. Ejecute el siguiente comando:

```bash
sudo pacman -S python-virtualenv
```

Ahora, cree un nuevo entorno virtual con nombre env con el siguiente comando:

```bash
virtualenv env
```

Ahora, active el entorno virtual con el siguiente comando:

```bash
source env/bin/activate
```

Ahora, instale Django con el siguiente comando:

```bash
pip install django
```

Ahora, puede verificar la versión de Django instalada con el siguiente comando:

```bash
python -m django --version
```

    ## Comandos Utiles

Como saber que paquetes tengo instalado

```bash
pip freeze --local
```


## Crear un proyecto

```bash
django-admin startproject project01
```

## Ejecutar el servidor

```bash
# Tener en cuenta que debemos estar en la carpeta del proyecto
python manage.py runserver
```

## Crear aplicaciones

Creamos una carpeta que se llame applications en nuestro proyecto

```
mkdir applications
```