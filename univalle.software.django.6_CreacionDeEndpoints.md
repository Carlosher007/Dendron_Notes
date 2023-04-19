---
id: 9wlnpj4se0qgziy4zdnuhzg
title: 6_CreacionDeEndpoints
desc: ''
updated: 1681149670159
created: 1680926895917
---

Nos ubicamos en inmuebles y luego en urls.py  y colocamos

```python
from django.urls import path, include
path('inmueble/', include('inmuebleslist_app.urls')),
```

Vamos a urls de inmueblelist_app y colocamos

```python
from django.urls import path
from inmuebleslist_app.views import inmueble_list 

urlpatterns = [
    path('inmueble/', inmueble_list, name='inmueble-list'),
]
```

Vamos a views.py de inmueblelist_app y colocamos

```python
from django.shortcuts import render
from inmuebleslist_app.models import Inmueble

# Create your views here.
def inmueble_list(request):
  inmueble = Inmueble.objects.all()
  data={
    'inmueble':list(inmuebles.values())
  }
  return JsonResponse(data)
```

## Buscar por id

 Vamos a urls de inmueblelist_app y colocamos

```python
urlpatterns = [
    path('inmueble/', inmueble_list, name='inmueble-list'),
    path('<int:pk>', inmueble_detalle, name='inmueble-detail'),
]
```

Vamos a views.py

```python
def inmueble_detalle(request, pk):
  inmueble = Inmueble.objets.get(pk=pk)
  data = {
    'direccion': inmueble.direccion,
    'pais': inmueble.pais,
    'imagen': inmueble.imagen,
    'activate': inmueble.activate,
    'descripcion': inmueble.descripcion,
  }
  return JsonResponse(data)
```
