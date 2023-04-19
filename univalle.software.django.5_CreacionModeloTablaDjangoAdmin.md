---
id: 23vdjvlipbri95b9xznlc9s
title: 5_CreacionModeloTablaDjangoAdmi
desc: ''
updated: 1680926483214
created: 1680926312092
---

> En nuestro archivo models.py de la aplicacion inmuebleslist_app, creamos la clase Inmueble, que hereda de la clase Model de Django, y le agregamos los atributos que queremos que tenga nuestra tabla en la base de datos

```python
class Inmueble(models.Model):
  direccion = models.CharField(max_length=50)
  pais = models.CharField(max_length=150)
  descripcion = models.CharField(max_length=500)
  imagen = models.CharField(max_length=900)
  activate = models.BooleanField(default=True)
  
  # Lo siguiente es para que cuando se muestre el objeto en el admin, se muestre el nombre de la direccion
  def __str__(self):
    return self.direccion  
```

> Ahora en nuestro archivo admin.py de la aplicacion inmuebleslist_app, importamos la clase Inmueble y la registramos en el admin de Django

```python
from inmuebleslist_app.models import Inmueble

# Register your models here.
admin.site.register(Inmueble)
```
> Hacemos el makemigrations para que se cree el archivo de migracion y el migrate para que se cree la tabla en la base de datos

```bash
python manage.py makemigrations
python manage.py migrate
```
