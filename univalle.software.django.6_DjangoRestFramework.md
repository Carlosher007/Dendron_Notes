---
id: ynd55bbwat3qn7zeqbhcpgm
title: 6_DjangoRestFramework
desc: ''
updated: 1681271085855
created: 1681149731541
---

Vamos a la consola y nos paramos en la carpeta del proyecto y ejecutamos el siguiente comando:

```bash
pip install djangorestframework
```

Django rest framework es un framework que nos permite crear apis rest de forma sencilla, que basicamente son endpoints que nos permiten hacer peticiones http y obtener respuestas en formato json.

Vamos a la carpeta del proyecto y abrimos el archivo settings.py y agregamos rest_framework en la lista de apps:

```python
INSTALLED_APPS = [
    'rest_framework',
]
```

> Serializacion: Es el proceso de convertir un **Comples Datatype** a **Python Native Datatype* para finalmente llevarlo a JSON data
> Deserializacion: Es el proceso cuando tenemos el JSON data y lo deserializamos para que sea **Python native datatype** y finalmente a **COmplex datatype** que es lo qu epodemos guardar en la BD

# Empezar la REST WEB API

En inmuebleslist_app creamos la carpeta api (crear estructura que de sopote a la api). Creamos los archivos: urls.py, viws.py.

Dentro de api escribimos:

```python
from django.urls import path
from inmuebleslist_app.api import inmueble_list, inmueble_detalle

urlpatterns = [
    path('inmuebles/', inmueble_list, name='inmueble_list'),
    path('<int:pk>', inmueble_detalle, name='inmueble_detalle'),
]
```

Dentro de api creamos serializers.py:

```python
from rest_framework import serializers+

class InmuebleSerializer(serializers.Serializer):
    id = serializers.IntegerField(read_only=True)
    direccion = serializers.CharField()
    pais = serializers.CharField()
    descripcion = serializers.CharField()
    imagen = serializers.CharField()
    active = serializers.BooleanField()
```

Con esto el urls.py a nivel de inmuebleslist_app ya no es necesario y lo podemos eliminar, así como las views.py que ya no son necesarias, por lo que comentamos todo su contenido.

Vamos a views.py dentro de api:

```python
from rest_framework.responde import Response
from inmuebleslist_app.models import Inmueble
from inmuebleslist_app.api.serializers import InmuebleSerializer
from rest_framework.decorators import api_view

@api_view() #GET
def inmueble_list(request):
    inmuebles = Inmueble.objects.all()
    #Objeto de data ya serializada
    serializer = InmuebleSerializer(inmuebles)

    #Retornamos en JSON
    return Response(serializer.data)

@api_view 
def inmueble_detalle(request, pk):
    inmueble = Inmueble.objects.get(pk=pk)
    serializer = INmuebleSerializer(inmueble)

    return Response(serializer.data)
```

Vamos al urls.py del manage.py, o mas bien dentro de la carpeta inicial. Y reemplazamos en urlpatters para que vaya a **inmuebleslist_app.api.urls**






