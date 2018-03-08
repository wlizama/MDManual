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