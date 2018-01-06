# Introducción al Lenguaje C

**Notas:**

+ El lenguaje ``C`` fue una revolución en su época ya que en ese entonces se utilizaba todavía el lenguaje ensamblador para acceder al lenguaje máquina o para trabajar directamente con el hardware.

+ Lo increíble de este lenguaje era que tenía la capacidad de trabajar a nivel hardware y además estaba optimizado pues era un lenguaje de alto nivel.

+ El lenguaje es hoy en día todavía el lenguaje de programación más utilizado en sistemas embebidos y en sistemas de bajos recursos de hardware donde necesitamos el acceso al hardware y donde se necesita tener muy alto rendimiento.

+ El lenguaje ``C`` tardó varios años en estandarizarse.

+ Un estándar en ``C`` significa una serie de guías y directivas que se deben de seguir al momento de escribir tu código que están respaldadas por una asociación (ANSI).

+ La programación estructurada es un método de programación o un paradigma que dice que vamos a ejecutar el código de forma secuencial, línea tras línea, del inicio al fin.

+ ``C`` es un lenguaje de programación compilado.

+ ``C`` es un lenguaje tipado.


## Características importantes de C
+ Núcleo del lenguaje simple que opera con bibliotecas.

+ Lenguaje flexible que soporta la programación.

+ Acceso a memoria de bajo nivel con punteros.

+ Utiliza un conjunto reducido de palabras clave.

+ Pasaje de parámetros por valor y referencia.

## Tipos de errores y datos en C
Existen 4 tipos principales de errores en C:

+ **Sintácticos:** Todo lenguaje tiene una estructura definida de instrucciones que vamos a utilizar para indicarle al programa lo que nosotros queremos hacer. Estos errores son cuando escribimos mal en el código estas instrucciones ya definidas.

+ **En el enlace:** Cuando enlazamos las librerías con nuestro código inicial, puede ocurrir que invoquemos mal una función o no insertemos la librería que necesitábamos, esto a la hora de compilar nos va a arrojar un error.

+ **De ejecución:** Este sucede cuando por alguna razón, mientras el programa está corriendo, alguno de los valores que vamos a utilizar en una variable, genera que haya una operación inválida.

+ **Semánticos:** Es mucho más complicado detectarlos, ya que son los errores que tenemos cuando nuestros programa funciona bien, se ejecuta bien, corre sin problemas técnicos pero no está teniendo el resultado que nosotros estábamos esperando y la solución no está bien implementada.


## Identificadores
Es el nombre que identifica una constante, variable o función.

Reglas para los identificadores:

+ Longitud ilimitada, pero se recomienda usar nombres descriptivos pero cortos.

+ Deben comenzar con una letra o guión bajo.

+ No se puede usar números.

+ No se puede usar caracteres especiales.

+ Deben ser únicos en el programa.

+ Énfasis en la diferencia entre mayúsculas y minúsculas.

+ No puede coincidir con una palabra reservada del lenguaje o con una función de biblioteca.


## Tipos de datos en C
+ **char** Caracter

+ **int** Número entero

+ **float** Número real de precisión simple

+ **double** Número real de precisión doble


## Variables en C
Las variables son una posición de memoria donde se almacena un dato.

Hay dos cosas que se deben definir en una variable:

**Nombre:** Esto nos sirve para poder recuperar su valor en cualquier parte del programa que estemos desarrollando.

**Tipo:** Es el límite que le damos de almacenamiento de valores.


## Operadores y expresiones
Son símbolos específicos que van a tener una función definida.

Los operadores se dividen en 4 tipos:

**Operadores de Asignación ( = ):** Este nos permite asignarle el resultado de una expresión a una variable dada. Es importante recordar que la expresión debe de usar los mismo tipos de datos que vamos a guardar en la variable.

**Operadores Aritméticos:** Estos operadores van a tener un orden o jerarquía en la que se resuelven, los paréntesis nos van a ayudar a que este orden se cumpla para llegar al resultado que se espera.

**Operadores Relacionales:** Estos nos van a servir para establecer una relación entre dos números y evaluarla o hacer una comparación.

**Operadores Lógicos:**

a) Siempre nos van a devolver valores en verdadero o falso, los cuales son denominados valores booleanos.

b) En el lenguaje de programación de C no existen los valores booleanos, por lo que así se definen:

- **Valor verdadero.** Cualquier número que sea distinto a cero.

- **Valor falso.** Cero.

- Lo convencional es que se utilice **1 para verdadero y 0 para falso.**

**Importante:**

+ Los operadores lógicos o booleanos son empleados para comparar dos valores.

+ Los operadores lógicos o booleanos denotan una relación entre dos valores.

+ Los operadores lógicos o booleanos tienen el mismo nivel de prioridad.
