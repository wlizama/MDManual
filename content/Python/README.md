# Python

Python es un lenguaje de programación creado por [Guido Van Rossum](http://en.wikipedia.org/wiki/Guido_van_Rossum), con una sintaxis muy limpia, ideado para enseñar a la gente a programar bien. Se trata de un lenguaje interpretado o de script.


## Tipo de datos
+ **Enteros (int):** en este grupo están todos los números, enteros y long.

+ **Booleanos (bool):** Son los valores falso o verdadero, compatibles con todas las operaciones booleanas ( and, not, or ) ``true, false``.

+ **Cadenas (str):** Son una cadena de texto.

+ **Listas:** Son un grupo o array de datos, puede contener cualquiera de los datos anteriores ``[ 1, 2, 3, "hola" , [ 1, 2, 3 ] ], [ 1, "Hola", True ]``.

+ **Diccionarios:** Son un grupo de datos que se acceden a partir de una clave ``{ "clave" : "valor" }, { "nombre" : "Fernando" }``.

+ **Tuplas:** también son un grupo de datos igual que una lista con la diferencia que una tupla después de creada no se puede modificar ``[ 1, 2, 3, "hola", [ 1, 2, 3 ] ], [ 1, "Hola", True ]``.

+ **Set:** Los sets son muy similares a las listas, pero estas no permiten elementos repetidos. Cuando trabajamos con sets, podemos realizar las operaciones básicas de conjuntos, esto quiere decir que se puede calcular los valores de intercepción, diferencia, unión.

```py
  # Declarar sets
  s = set([1,2,3])
  t = set([3,4,5])

  # Operaciones con sets
  s.union(t)      # set([1,2,3,4,5])
  s.difference(t) # set([1,2])
  t.difference(s) # set([4,5])

```

## Operadores Matematicos
Los operadores nos permiten trabajar con valores y generar nuevos valores por medio de estas operaciones.

Existen muchos operadores básicos,

+ (+) Suma

+ (-) Resta

+ (asterisco) Multiplicación

+ (/) División

+ (//) División de enteros

+ (%) Operador de módulo

+ (doble asterisco) Potencias

+ (>) Mayor que

+ (<) Menor que

+ (==) Igual

+ (>=) Mayor igual

+ (<=) Menor igual


## Funciones
Las funciones las defines con _**def**_ junto a un nombre y unos paréntesis que reciben los parámetros a usar. Terminas con dos puntos.

Después por indentación colocas los datos que se ejecutarán desde la función:

```py
  def my_first_function(self):
    return "Hola con Python 👋"
```

## Estructuras de Control

+ **Condicional IF**

Los condicionales tienen la siguiente estructura. Ten en cuenta que lo que contiene los paréntesis es la comparación que debe cumplir para que los elementos se cumplan.

```py
  if ( a > b ):
    elementos 
  elif ( a == b ): 
    elementos 
  else:
    elementos
```

+ **Bucle FOR**

El bucle de for lo puedes usar de la siguiente forma: recorres una cadena o lista a la cual va a tomar el elemento en cuestión con la siguiente estructura:

```py
  for i in range(10):
    print i
```

+ **Bucle WHILE**

En este caso while tiene una condición que determina hasta cuándo se ejecutará. O sea que dejará de ejecutarse en el momento en que la condición deje de ser cierta

```py
  while x < 10: 
   print x 
   x += 1
```

## Dictionary comprehension - List comprehension
Dictionary comprehension y list comprehension nos permite escribir listas o diccionarios de forma más sencilla.

```py

  ### Números Pares
  pares = []
  for num in range(1,31):
      if num % 2 == 0:
          pares.append(num)


  # Esto mismo lo podemos expresar con una list comprehension
  pares = [num for num in range(1,31) if num % 2 == 0]

```

## Entorno virtual en Python

En Python la comunidad comparte su código usando PyPi (_python package index_), es un repositorio para instalar módulos de la comunidad.

Con ``pip install <nombre>`` se puede instalar el paquete que deseas.

Podemos utilizar requirements.txt para ordenar los paquetes que requiere tu proyecto.

### Ambiente virtual Python

Nos permite encapsular un proyecto para poder instalar las versiones de los paquetes que se requieran sin tenerlos que instalar en todo el sistema operativo.

**Crear un entorno virtual**

1. Dentro de la carpeta de tu proyecto ejecutas

```sh
  virtualenv venv
```

2. Encender un entorno virtual

```sh
  source venv/bin/activate
```

3. Ver las dependencias instaladas en el entorno virtual

```sh
  pip freeze
```

4. Instalar dependencias del archivo requirements
```sh
  pip install -r requirements.txt
```

---

## Enlaces de interés

+ [Documentación oficial de Python](https://docs.python.org/3/whatsnew/3.6.html)

+ [Paquetes Python](https://pypi.org/)

+ [PEP Estilo de codificación](https://www.python.org/dev/peps/pep-0008/)