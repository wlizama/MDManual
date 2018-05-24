# Algoritmos con C

## Lenguajes de programación
Hay dos tipos de lenguajes de programación que hoy en día ya son poco usados:

**Lenguaje de máquina:** Codigo binario o hexadecimal directamente interpretados por el microprocesador de el computador difíciles de leer para una persona.

**Lenguaje ensamblador:** Utiliza instrucciones que son específicas del CPU y que tienen una traducción directa al Hardware que lo compone.

Los lenguajes de programación que actualmente son los que se utilizan son:

**Lenguaje de bajo nivel:** Va a ser un lenguaje que está muy cerca de lo que se interpreta directamente en el computador.

**Lenguaje de alto nivel:** Son con los que estamos programando cosas como la Web, grandes aplicaciones, etc.

**Notas:**

- Las computadoras trabajan con 0 y 1, donde los transistores pueden tener diferentes estados por ser materiales semi conductores. Esto es utilizado por medio de electrónica para que los circuitos combinen y puedan funcionar haciendo operaciones.

- Si tratamos de ver desde el procesador las operaciones que se ejecutan en la computadora, sería nada comprensible, tendríamos que hacer una serie de códigos binarios y hexadecimales (lenguaje máquina) que hoy en día ya nadie hace.

- El lenguaje ensamblador lo proporciona el fabricante del microcontrolador.

- El chip de un Arduino se puede programar todavía con un ensamblador.

- Entre más bajo se el nivel de un lenguaje de programación, más directo va a ser para trabajar con el Hardware.

- Los lenguajes de alto nivel permiten a los programadores tener una interacción mucho más fácil con equipos, son lenguajes que son mucho más parecidos al inglés.

- Los lenguajes de alto nivel están muy alejados del Hardware, por lo que casi siempre van a contar con un intérprete que se va a encargar de traducirlo al lenguaje ensamblador o al código máquina, que va a ser el código final que se va a ejecutar en nuestros equipos.

- Existen lenguajes de programación que no son tipados, es decir, no van a tener ningún tipo de dato dentro de su estructura.

- Lo que sucede con un lenguaje de programación que no tiene tipo de datos es que no va a ser tan fácil optimizar el uso de recursos.

## Algoritmo
Un algoritmo es un conjunto de instrucciones finitas que nos permiten resolver un problema dado paso a paso y sin generar ambigüedades.

## User defined data types: Estructuras de datos y custom data types
En algunas ocasiones, cuando estamos programando, no nos basta con los tipos de datos definidos por el lenguaje previamente, para esto podemos ir definiendo nosotros un tipo de dato propio que vayamos a estar usando en nuestro proyecto.

**Ejemplo:** En el lenguaje de programación de ``Java``, esto se conoce como clases. Así mismo en el lenguaje de ``C++`` o ``C`` se conoce como estructuras.

### Razones por las que podemos crear nuestro propio tipo de dato:
Se tiene mucha más flexibilidad en el proyecto.
Permite tener un mejor uso de memoria, porque estamos definiendo al programa una serie de pasos en los que no va a tener que procesar nada.

### ¿Qué son las estructuras de datos?
Las estructuras de datos son una manera eficiente de organizar y almacenar la información que estamos recibiendo.

### Estructuras de datos comunes:
+ Listas
+ Arreglos
+ Listas ordenadas
+ Árboles

**Tipos de datos abstractos:** Tipo de datos definido por el usuario con un operador que se va a utilizar en aplicaciones.

## Estructuras de control y estructuras de control secuenciales
Nos van a permitir definir el flujo de nuestro programa, ejecutar acciones en la parte del proceso correcta.

### Tipos de Estructuras de Control:

+ **Estructuras Secuenciales:** Son las más básicas, funciona como su nombre lo dice, en secuencia. El programa ejecuta los pasos ordenadamente uno tras otro hasta obtener el resultado y termina.

+ **Estructuras de control selectivas:** Nos van a permitir que nuestro algoritmo o el programa tome decisiones en el caso de ejecutar un pedazo de código o un segmento de código o no con base en una condición específica que debemos verificar si se cumple, y si se cumple ejecutamos la condición y si no, se va colocando lo siguiente de nuestro código.

    + Si, **if**. Aquí vamos a tener una condición, y en caso de que la condición se cumpla vamos a ejecutar un pedazo de código. En caso de que la condición no se cumpla vamos a saltar ese pedazo de código.

    + Si - sino, **if - else**. Nos permite una condición y bifurcar el camino para dos rutas distintas, es decir, si la condición se cumple, ejecutamos una acción y si la condición no se cumple ejecutamos otra acción diferente.

    + Si, sino entonces… sino, **if, else if, else**. Aquí vamos a poder verificar la primera condición, en caso de que esta primera no se cumpla, podemos verificar una segunda condición y en caso de que esta segunda no se cumpla, podemos tener _n_ condiciones. Si este número _n_ que hayamos determinado no se cumplen, al final se ejecutará else (sino).

+ **Estructuras de control repetitivas:** Estás nos van a permitir crear bucles donde nuestros programas va a estar repitiéndose hasta que una condición les indique lo contrario o mientras una condición les indique que hagamos eso.

    + Mientras, **while**. Mientras una condición se cumpla, nosotros vamos a ejecutar todo el código que está dentro de este ciclo y vamos a repetirlo.

    + Haz mientras, **do while**. Esta instrucción nos permite entrar por lo menos una vez a ejecutar el código que está dentro de esta instrucción y si la condición se cumple , entonces repetimos, pero si la condición no se cumple salimos del código.

    + Para, **for**. Se utiliza cuando necesitamos repetir una serie de veces definida un código.

## Cómo comparar algoritmos y ritmo de crecimiento
Debemos saber que existen buenas y malas métricas para comparar algoritmos.

**Malas métricas:**

+ **Tiempo de ejecución:** El tiempo de ejecución va a variar dependiendo del equipo donde se ejecute el algoritmo.
+ **Número de instrucciones ejecutadas:** Una vez tenemos un algoritmo hecho, debemos llevarlo a un lenguaje de programación, lo que significa que va a depender del lenguaje que estemos, el número de líneas de código (instrucciones) que vamos a utilizar.

_**Para hacer un análisis del ritmo de crecimiento, siempre vamos a tomar el término de mayor peso.**_

---

## Enlaces de interés

+ [Documentación de C](https://devdocs.io/c/)

