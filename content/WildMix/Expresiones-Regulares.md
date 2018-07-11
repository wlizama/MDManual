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

## El caso de (?) como delimitador

Busca el carácter precedente 0 (cero) o 1 (una) vez. Es equivalente a ``{0,1}``.

Por ejemplo, la expresión ``/e?le?/`` encontrará la subcadena '**el**' en la cadena "**angel**" y la subcadena '**le**' en la cadena "**abominable**" y también el carácter '**l**' en la cadena "**muslo**".

Si se utiliza inmediatamente después que cualquiera de los cuantificadores ``*, +, ?, o {}``, hace que el cuantificador no sea expansivo _(encontrando la menor cantidad posible de caracteres), en comparación con el valor predeterminado, que sí es expansivo (encontrando tantos caracteres como le sea posible)_. Por ejemplo, aplicando la expresión ``/\d+/`` a la cadena "123abc" encuentra "123". Pero aplicando la expresión ``/\d+?/`` a la misma cadena, encuentra solamente el carácter "**1**".

También se utiliza en coincidencias previsivas.

## Principio (^) y final de linea ($)

``^`` Coincide con el comienzo de la cadena, o el comienzo de una línea si la bandera multilínea **(m)** está habilitada

``$`` Coincide con el final de la cadena, o al final de una línea si la bandera multilínea **(m)** está habilitada


## Clases comunes

``\t`` Representa un tabulador.

``\r`` Representa el _"retorno de carro"_ o _"regreso al inicio"_ o sea el lugar en que la línea vuelve a iniciar.

``\n`` Representa la _"nueva línea"_ el carácter por medio del cual una línea da inicio. Es necesario recordar que en Windows es necesaria una combinación de ``\r\n`` para comenzar una nueva línea, mientras que en Unix solamente se usa ``\n`` y en _Mac\_OS clásico_ se usa solamente ``\r``.

``\a`` Representa una _"campana"_ o _"beep"_ que se produce al imprimir este carácter.

``\e`` Representa la tecla <kbd>Esc</kbd> o <kbd>Escape</kbd>

``\f`` Representa un salto de página

``\v`` Representa un tabulador vertical

``\x`` Se utiliza para representar caracteres **ASCII** o **ANSI** si conoce su código. De esta forma, si se busca el símbolo de derechos de autor y la fuente en la que se busca utiliza el conjunto de caracteres _Latin-1_ es posible encontrarlo utilizando **"\xA9"**.

``\u`` Se utiliza para representar caracteres Unicode si se conoce su código. **"\u00A2"** representa el símbolo de centavos. No todos los motores de Expresiones Regulares soportan Unicode. El _.Net Framework_ lo hace, pero el _EditPad Pro_ no, por ejemplo.

``\d`` Representa un dígito del **0** al **9**.

``\w`` Representa cualquier carácter alfanumérico.

``\s`` Representa un espacio en blanco.

``\D`` Representa cualquier carácter que no sea un dígito del **0** al **9**.

``\W`` Representa cualquier carácter no alfanumérico.

``\S`` Representa cualquier carácter que no sea un espacio en blanco.

``\A`` Representa el inicio de la cadena. No un carácter sino una posición.

``\Z`` Representa el final de la cadena. No un carácter sino una posición.

``\b`` Marca la posición de una palabra limitada por espacios en blanco, puntuación o el inicio/final de una cadena.

``\B`` Marca la posición entre dos caracteres alfanuméricos o dos no-alfanuméricos.


## Expresiones comunes

**Validación de URL**

```
  https?:\/\/[\w\-\.]+\.\w{2,6}\/?\S*
```

**e-mail**

```
  [\w\._]{5,30}\+?[\w]{0,10}@[\w\.\-]{3,}\.\w{2,5}
```

---

## Enlaces de interés

+ [Leer, construir y testear expresiones regulares](https://regexr.com/)

+ [Testear online expresiones regulares](https://regex101.com/)

+ [Expresiones regulares https://developer.mozilla.org](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Regular_Expressions)