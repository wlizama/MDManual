# Abstracción

Una abstracción puede definirse como:

>**las características especificas de un objeto, aquellas que lo distinguen de los demás tipos de objetos y que logran definir límites conceptuales respecto a quien está haciendo dicha abstracción del objeto.**

Una abstracción se enfoca en la visión externa de un objeto,  separa el comportamiento  específico de un objeto, a esta división que realiza se le conoce como la **barrera de abstracción**, la cuál se consigue aplicando el principio de **mínimo compromiso**.

Pero… _¿Qué es el principio de mínimo compromiso?_ Se refiere al proceso por el cuál la **interfaz** de un objeto muestra su comportamiento específico y nada más, absolutamente nada más.

Pero… _¿Qué es una Interfaz?_ Una interfaz de objeto permite crear código con el cuál se específica que métodos serán implementados por una clase sin necesidad de definir que harán estos métodos, dichos métodos deben ser públicos.

Pero… Existe también el principio de mínima sorpresa, en el cuál una abstracción obtiene el comportamiento **completo** de algún objeto y por ende no ofrece sorpresas o efectos laterales que lleguen más allá del ámbito de la abstracción.

Hay una alta gama de abstracciones que existen desde los objetos que modelan muy cerca de entidades, a objetos que no tienen razón para existir, vamos a hacer una rápida mención de ello.

**Abstracción de Entidades**: Es un objeto que representa un modelo útil de una entidad que se desea.

**Abstracción de Acciones**: Un objeto que representa un conjunto de operaciones y todas ellas desempeñan funciones del mismo tipo.

**Abstracción de Máquinas virtuales**: Un objeto que agrupa operaciones, todas ellas virtuales, utilizadas por algún nivel superior de control u operaciones (entre ellos podríamos hablar de un circuito).

**Abstracción de coincidencia**: Un objeto que almacena un conjunto de operaciones que no tienen relación entre sí.

## Modelo contractual de programación

En dicho modelo podemos mencionar que la vista exterior de cada objeto define una interfaz del que puedan depender otros objetos, esta interfaz como bien lo habíamos mencionado, establece todas las suposiciones que pueda hacer un objeto cliente acerca del comportamiento de un objeto servidor, es decir la interfaz abarca las responsabilidades de un objeto, dicho en otras palabras, abarca el comportamiento del que se le considera responsable.

Un objeto puede actuar y reaccionar de diferentes formas, un conjunto de operaciones que puede realizar un cliente sobre un objeto se le denomina **protocolo**.

No está demás mencionar que toda abstracción tiene propiedades **estáticas** y **dinámicas**.

**Propiedades estáticas** podemos mencionar, el nombre, el tamaño, en algunas ocasiones su contenido.

**Propiedades dinámicas** podemos mencionar  peso, tamaño, contenido.

Dependiendo el contexto que se esta analizando el contenido u otras propiedades pueden ser dinámicas como estáticas.

Realizaremos un breve ejemplo de una abstracción sobre un vehículo.

Supongamos qué en este ejemplo nos están solicitando la abstracción de un vehículo en cuanto a su comportamiento.

La pregunta que hago es ¿Cuales son los comportamientos que tienen todos los vehículos? con base a esta pregunta, automáticamente fluye nuestra abstracción del comportamiento de un vehículo.

1. Encender Vehículo
2. Apagar Vehículo
3. Acelerar Vehículo
4. Frenar Vehículo
5. Retroceder Vehículo
6. Parabrisas Vehículo

y podría listar el comportamiento del vehículo, ahora para que ustedes puedan ejercitar lo aprendido, pueden realizar abstracciones de objetos, incluyendo sus características y el comportamiento.

---

[:arrow_backward: Abstracción](https://github.com/wlizama/MDManual/blob/master/content/POO/Lesson_3.md) | [:book: Indice POO](https://github.com/wlizama/MDManual/tree/master/content/POO) | [:arrow_forward: Encapsulamiento](https://github.com/wlizama/MDManual/blob/master/content/POO/Lesson_3.md)
|--- | --- | --- |