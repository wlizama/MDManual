# Tipos de datos

Un tipo de dato indica un conjunto de valores que significan lo mismo , hay algunos tipos que no representan valores en la aplicación que se ejecutan.

Los tipos son la puesta en vigor de la clase de objetos, los objetos con distintos tipos no podrán intercambiarse o al menos no totalmente, si se lograran intercambiar solo de formas muy limitadas.

>**Un tipo es una caracterización de propiedades estructurales o de comportamiento que utilizan una serie de entidades.**

Tengamos en cuenta que la buena comprobación de tipos nos impide que se mezclen abstracciones.

Existen 3 maneras de comprobar los tipos: **estático**, **dinámico**, **estricto**, este último casi siempre suele tomarse como tipo estático.

## ¿En qué consiste el tipo Estático?

Consiste en qué el tipo exacto de cada expresión pueda ser localizado en tiempo de compilación mediante un análisis estático de la aplicación.

El tipo estático detecta anomalías en tiempo de compilación, pero puede ser muy restrictivo.

Entre los lenguajes que utilización tipado estático podemos mencionar, Java o C++.

**¿Por qué ellos?**

Porqué estos permiten que los errores sean detectados antes de la ejecución, haciendo así la aplicación más eficiente.

## ¿En qué consiste el tipo Estricto?

Todas las expresiones de los tipos deben de ser consistentes en tiempo de compilación.

Dejando más claro los tipos de datos estrictos aseguran que no se asignen accidentalmente un tipo de valor incorrecto o una variable.

Este tipo de datos también asegura que no se acceda a propiedades o métodos que no formen parte de dicho tipo de objeto.

Pero... **¿Qué es la Consistencia?**

La consistencia es la cualidad que tiene un objeto que resiste sin corromperse fácilmente.

La consistencia se define a traves de tres restricciones fundamentales.

+ **Restricción de declaración:** Indica que todos las entidades deben tener un tipo declarado.

+ **Restricción de Compatibilidad:** El tipo fuente debe ser compatible con el tipo de destino.

+ **Restricción de llamada a característica:** Para poder llamar a un atributo o clase X desde la clase Y, X tiene que estar definida en y en sus antecesores.

### Pesimismo

Se llama así cuando se tienen operaciones con tipos las cuales creemos estar seguros que funcionaran o serán válidas siempre, pero si no se tiene dicha seguridad, entonces es mejor que no se permitan.

Un ejemplo de Pesimismo sería, una Clase _**Animal**_, una clase **perro** que tiene le método correr.

Qué sucedería si yo hago lo siguiente:

>**Animal _UnAnimal_ = agregue un perro
luego tomo la variable _UnAnimal_ y hago uso del método correr (UnAnimal.correr)**

Esto funcionaría si todos los Animales corrieran ¿pero qué pasa si yo en _UnAnimal_ agrego un **perico**?

Para este problema tenemos un par de soluciones una de ellas llamada el **Type-Cast o Run-Time Type Information**.

## ¿En que consiste el tipo Dinámico?

Se realizan las comprobaciones en tiempo real (ejecución).

Esto quiere decir que una variable puede tomar valores de diferentes tipos en diferentes momentos.

Entre los lenguajes que podemos mencionar que utilizan este tipado está **Phyton** y **PHP**.

### ¿A qué se refiere el término fuertemente tipado?

Esto nos exige tratar un tipo de dato solamente como ese mismo tipo, no permite conversiones incluidas, las conversiones de datos son explicitas.

Un lenguaje fuertemente tipado no permite tratar un tipo de dato como otro, no permiten violaciones de los tipos de datos, es decir, un tipo concreto no se puede usar como si fuera un tipo diferente a menos que se haga una _conversión_.

La mayoría de estos lenguajes realiza la conversión implícitamente.

### ¿A qué se refiere el término débilmente tipado?

Se refiere a las conversiones incluidas que se realizan, por ejemplo si se quiere convertir un real a entero, podría redondear el decimal a entero, quitar los decimales o mostrar solo el entero, esto depende de como trate la conversión el lenguaje débilmente tipado que se esté utilizando.

El tipo de dato no se define sobre la variable, si no que se define sobre el valor, debido a esto se puede usar variables de cualquier tipo en un mismo escenario.

Gracias a esto podemos mencionar que Phyton es un lenguaje de tipo dinámico (porqué no es necesario especificar el tipo de dato) y débilmente tipado (porqué una variable puede tomar distintos tipos de datos.

---

[:arrow_backward: Jerarquía](https://github.com/wlizama/MDManual/blob/master/content/POO/5-Jerarquia.md) | [:book: Indice POO](https://github.com/wlizama/MDManual/tree/master/content/POO) | [Concurrencia y Persistencia :arrow_forward:](https://github.com/wlizama/MDManual/blob/master/content/POO/7-Concurrencia-y-Persistencia.md)
|--- | --- | --- |
