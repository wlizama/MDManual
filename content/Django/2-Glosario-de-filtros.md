# Glosario de filtros

## contains / icontains

Es un filtro que se aplica a texto, te dice si el argumento que le pasas esta contenido en el. Su variacion, **icontains** hace una busqueda ignorando si las letras son mayusculas/minusculas.

A nivel de base de datos funciona como un _like_, algo importante a tener en cuenta es que puede ser muy lento en _textfields_ de gran contenido, con este filtro puedes hacer buscadores sencillos.

```py
  Country.objects.get(name__contains='co')
```

## in

Es un filtro que verifica si el valor esta dentro de la lista, es posible pasarle otros queries.

```py
  Entry.objects.filter(id__in=[1, 3, 4])
```

## gt / gte / lt / lte

Son los filtros correspondientes a _mayor que_**(gt)**, _mayor igual que_**(gte)**, _menor que_**(lt)**, y _menor o igual a_**(lte)**

Estos filtros funcionan com valores escalares, y con fechas.

```py
  Person.objects.filter(age__gte=25) # edad mayor o igual a 25
  Person.objects.filter(age__lte=25) # edad menor o igual a 25
  Person.objects.filter(age__lt=25)  # edad menor a 25
  Person.objects.filter(age__gt=25)  # edad mayor a 25

```

## range

Determina si una fecha esta dentro de un rango.

```py
  from datetime import datetime, timedelta
  from_date = datetime.now() - timedelta(days=20)
  to_date = datetime.now() - timedelta(days=10)
  User.objects.filter(date_joined__range=(from_date, to_date))
```

## isnull

Determina si el campo es nulo.

```py
  Entry.objects.filter(pub_date__isnull=True)
```

## year/month/day/week

Para las fechas, podemos preguntar por un dato en especifico, por año, mes, dia, semana.

```py
  User.objects.filter(date_joined__year=2018) # Filtra por el año 218
  User.objects.filter(date_joined__month=12)  # Filtra por el mes 12
  User.objects.filter(date_joined__day=1)     # Filtra por el dia 1
  User.objects.filter(date_joined__week=1)    # Filtra por la semana 1
```

Puedes contatenar los filtros comparadores, es decir puedes hacer ``date_joined__year__gte=2018``