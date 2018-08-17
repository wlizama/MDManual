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

## Lambdas
Lambdas son funciones de una línea. También se conocen como funciones anónimas en algunos otros idiomas. Es posible que desee utilizar lambdas cuando no desee utilizar una función dos veces en un programa. Son como las funciones normales e incluso se comportan como ellos.


Simple suma: 
```py
  suma = lambda x, y: x + y

  print(suma(3, 5))
  # Output: 8
```

Ejemplo real:
```py
  a = [(1, 2), (4, 1), (9, 10), (13, -3)]
  a.sort(key=lambda x: x[1])

  print(a)
  # Output: [(13, -3), (4, 1), (1, 2), (9, 10)]
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

### PIP commands

Busqueda limitada de paquetes:

```sh
  ➜  python-training $ pip search xls

  xls (0.1.1)                                                     - XLS Parsing (from js-xls)
  pyexcel-xls (0.5.7)                                             - A wrapper library to read, manipulate and write data in xls format. Itreads xlsx and xlsm format
  xml-xls-loader (0.0.1)                                          - Module to load a MS xml xls into a pandas DataFrame
  odoo8-addon-account-balance-reporting-xls (8.0.1.0.0.99.dev19)  - Account balance reporting to XLS
  odoo8-addon-account-financial-report-webkit-xls (8.0.1.0.0)     - Add XLS export to accounting reports
  metzoo-python-parser-xls-consumo-puan-plugin (0.0.2)            - Python Puan energy report XLS parser Pluigin for Metzoo
  django-export-xls (0.1.1)                                       - A simple Django app to export data to an excel file.
  django-trackmodels-xls-ritual (0.0.3)                           - XLSX report plugin for django-trackmodels-ritual
  odoo8-addon-report-xls (8.0.0.6.1.99.dev12)                     - Excel report engine
  pydap.responses.xls (0.1.2)                                     - XLS response for Pydap
  icemac.ab.importxls (2.3.post1)                                 - Import XLS files into icemac.addressbook.
  django-po2xls (0.4.0)                                           - Convert gettext .po files to .xls
  FromXLS2CSV (1.4.2)                                             - Conversor de archivos XLS a CSV
  gif2xls (0.2.2)                                                 - Convert GIF images into XLS files.
  list2excel (0.5.6)                                              - Django XLS export made easy
  make_excel (1.2.0.dev1)                                         - Create .xls file with Python dictionary
  odoo8-addon-account-asset-management-xls (8.0.0.1.0.99.dev28)   - Assets Management Excel reporting
  odoo8-addon-account-journal-report-xls (8.0.0.2.0.99.dev22)     - Financial Journal reports
  odoo8-addon-mrp-bom-structure-xls (8.0.1.0.0)                   - Export BOM Structure to Excel
  docraptor (1.2.0)                                               - A wrapper for the DocRaptor HTML to PDF/XLS service.
  ...
```

Se puede instalar la última versión de un paquete especificando el nombre del paquete:

```sh
  ➜  python-training $ pip install novas

  Collecting novas
    Downloading novas-3.1.1.3.tar.gz (136kB)
  Installing collected packages: novas
    Running setup.py install 
  for
    novas
  Successfully installed novas-3.1.1.3
```

También se puede instalar una verisón específica de un paquete ingresando el nombre del paquete seguido de ``==`` y el número de versión:

```sh
  ➜  python-training $ pip install requests==2.6.0

  Collecting requests==2.6.0
    Using cached requests-2.6.0-py2.py3-none-any.whl
  Installing collected packages: requests
  Successfully installed requests-2.6.0
```

Mostrar información de un paquete en particular:

```sh
  (venv) ➜  python-training $ pip show flask
  
  Name: Flask
  Version: 0.12.2
  Summary: A microframework based on Werkzeug, Jinja2 and good intentions
  Home-page: http://github.com/pallets/flask/
  Author: Armin Ronacher
  Author-email: armin.ronacher@active-4.com
  License: BSD
  Location: /home/wilder/Compartido/python-training/servidor/venv/lib/python3.5/site-packages
  Requires: Werkzeug, Jinja2, itsdangerous, click
  Required-by: 
```

Mostrar todos los paquetes instalados en el entorno virtual:

```sh
  (venv) ➜  python-training $ pip list

  beautifulsoup4 (4.5.3)
  pip (9.0.1)
  requests (2.13.0)
  setuptools (38.5.2)
  wheel (0.30.0)
```

Colocar en lista requirements.txt los paquetes instalados

```sh
  (venv) ➜  python-training $ pip freeze > requirements.txt

  Pillow==5.2.0
  reportlab==3.5.1
```

---

## Enlaces de interés

+ [Documentación oficial de Python](https://docs.python.org/3/whatsnew/3.6.html)

+ [Paquetes Python](https://pypi.org/)

+ [PEP Estilo de codificación](https://www.python.org/dev/peps/pep-0008/)