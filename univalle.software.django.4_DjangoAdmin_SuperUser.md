---
id: u1l8zsfm95faol149qlyuou
title: 4_DjangoAdmin_SuperUser
desc: ''
updated: 1680926289513
created: 1680924554292
---

> En nuestra carpeta del proyecto ( a nivel del manage.py ) ejecutamos el comando para la mirgracion, que no es mas que la creacion de la base de datos

```bash
python manage.py migrate
```

> Ahora creamos un super usuario para poder acceder al panel de administracion de Django

```bash
python manage.py createsuperuser
```

A este super usuario le pedira un nombre de usuario, un correo electronico y una contraseña

