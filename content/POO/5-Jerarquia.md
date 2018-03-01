# Jerarquía

Las abstracciones definen el comportamiento general de un “objeto”, en programación orientada a objetos, estas abstracciones pueden ordenarse y clasificarse, a esto se le conoce como Jerarquia.

Vamos a centrarnos en las dos jerarquías más importantes: **la relación de clases y relación de objetos**.

La relación de clases es a lo que llamamos **Herencia**.

**La herencia simple es la relación de clases más importantes**, es esencial en los sistemas orientados a objetos, recordemos que la herencia define una relación entre clases en la que una de ellas brinda la estructura de comportamiento definida en una o más clases.

Recordando que la herencia representa una jerarquía de abstracciones en la que una subclase hereda de una o más **superclases**.

ya habíamos escrito anteriormente de esto, una herencia denota una relación **<< es un >>** mencionemos algunos ejemplos:

>**Un Perro ES UN mamifero, Notesé que perro es una subclase de la superclase mamifero.
 Un gato ES UN  mamifero.**

La herencia implica una relación de **especialización** en la que la subclase especializa el comportamiento o la estructura más general de sus **superclases**.

En el ejemplo anterior, podemos observar que la clase _**perro**_ especializa a la clase _**mamifero**_, sabemos que todos los mamiferos “lactan”, pero la clase perro le esta dando la especialidad de que ese mamifero _**ladrá, muerde, etc**_.

**Herencia Múltiple:** Como su nombre lo indica, se refiere a la característica en la que una  clase puede heredar comportamientos de una o más **superclases**.

_Ejemplo:_

+ SubClase perroCocker:
  + Características: travieso, juguetón
+ SuperClase Perro:
  + Características: Ladrar, aullar, etc.
+ SuperClase Volador
  + Características: iniciarVuelo, iniciarAterrizaje, etc..

Ahora bien, si la Subclase PerroCocker heredara de ambas superclases (Perro y Volador), obtendríamos qué:

Un PerroCocker, es un perro volador.

>**NOTA: No todos los lenguajes orientados a objetos soportan la Herencia Multiple**

La Relación de Objetos esta relación se enfoca en la abstracción de la vida real de un objeto, esta relación denota el **<< parte de >>**, esto permite hablar de niveles de abstracción altos y bajos, los cuales indican la dependencia de una clase a otra.

Una clase tiene un nivel más alto de abstracción que cualquiera de las clases que dependen de ella.

_Ejemplo:_

Una llanta es **<< parte de >>** un carro.

pero tambien es <**< parte de >>** una moto, un camión, etc.

---

[:arrow_backward: Modularidad](https://github.com/wlizama/MDManual/blob/master/content/POO/4-Modularidad.md) | [:book: Indice POO](https://github.com/wlizama/MDManual/tree/master/content/POO) | [Tipos de datos :arrow_forward:](https://github.com/wlizama/MDManual/blob/master/content/POO/Tipos-de-datos.md)
|--- | --- | --- |
