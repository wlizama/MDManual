# Expresiones Regulares

Las expresiones regulares intentan solucionar problemas del día a día. Se intenta buscar la forma en que ciertos datos son presentados, por ejemplo un número de teléfono dependiendo de país y zona, tiene determinada cantidad de números, a veces separados con guiones o puntos, pero la estructura siempre es la misma

Otro ejemplo de uso de expresiones regulares sería intentar cambiar en un _.csv_ los precios de modo europeo a modo americano

Un dígito se puede expresar con ``/d``

Caracter de palabra: ``/w``

**Cadena de Caracteres**: Es un carácter _ASCII_ generalmente, seguido de otro carácter y de otro. No todos son visibles, el espacio por ejemplo. Cada carácter es un carácter.

## El caracter (.)

Encuentra todo lo que sea un carácter, coincide con cualquier carácter excepto fin de linea.

## Las clases predefinidas y construídas

Las búsquedas en las expresiones regulares funcionan en múltiplos de la cantidad de caracteres que explícitamente indicamos

**Dígitos:**

Encuentra todos los dígitos de 0 a 9.
    
``\d`` es equivalente a poner [0-9].
    
Si en vez de ``\d``, usamos por ejemplo ``[0-2]`` nos encontrará solamente los dígitos de 0 a 2.

Podemos usar ``\D`` para encontrar justo lo contrario, todo lo que no son dígitos.

**Palabras:**

Encuentra todo lo que puede ser parte de una palabra, tanto letras (minúsculas o mayúsculas) como números.

``\w`` es equivalente a poner ``[a-zA-Z0-9_]``.

Si en vez de ``\w``, usamos por ejemplo ``[a-zA-Z]`` nos encontrará solamente las letras.

Podemos usar ``\W`` para encontrar justo lo contrario, todos los caracteres que no son parte de palabras.

**Espacios:**

``\s`` encuentra todos los espacios (los saltos de línea también son espacios).

Podemos usar ``\S`` para encontrar justo lo contrario, todo lo que no son espacios.

## Los delimitadores: \+, \*, ?

``*`` Cero o muchos

``+`` Uno o muchos

``?`` Cero o uno

Ejemplos:

- ``\d+[a-z]``  Encuentra todo lo que tenga uno o más dígitos y al final tiene una letra.

- ``\d*[a-z]``  Encuentra todo lo que teniendo dígitos o no, al final tiene una letra.

## Los Contadores {n,m}

Donde ``n`` y ``m`` son enteros positivos y ``n <= m``. Coincide con al menos ``n`` y no más de ``m`` ocurrencias de la expresión. Si se omite ``m``, no tiene limite de máximo.

Por ejemplo, ``/a{1,3}/`` no coincide con "**cndy**", pero sí con la '**a**'' en "**candy**", las primeras 2 a en "**caandy**" y las primeras 3 a en "**caaaaaaandy**". Note que en "**caaaaaaandy**", la coincidencia es "**aaa**", aunque la cadena contenga más a en ella.