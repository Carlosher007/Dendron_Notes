---
id: 5f7ajczik88ksyopzondia2
title: 2_CrearEntorno
desc: ''
updated: 1680923926028
created: 1680043710559
---
Repasemos un poco lo que tenemos que hacer para crear entornos en django

> Estando en nuestra carpeta entornos ejecutamos el siguiente comando

```bash
virtualenv <<nombreEntorno>>
python -m venv <<nombreEntorno>>
```
> Ahora, active el entorno virtual con el siguiente comando:

```bash
source <<carpetaEntorno>>/bin/activate
```

> Para desactivar el entorno virtual, ejecute el siguiente comando:

```bash
deactivate
``` 

> Saber que paquetes tengo instalado

```bash
pip freeze
```