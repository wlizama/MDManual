# Concurrencia y Persistencia

La Concurrencia permite que distintos objetos actúen al mismo tiempo, usando diferentes hilos de control (un solo proceso).

>Es la propiedad que diferencia a los objetos entre estar activos o no.

Es muy común tener que manejar varias acciones diferentes al mismo tiempo, para ello se utilizan procesos los cuales producen acciones dinámicas independientes dentro de un sistema.

Sabemos que se tienen sistemas los cuales ejecutan en múltiples **CPU** permitiendo así hilos de control verdaderamente concurrentes, mientras que en los sistemas que ejecutan en un solo **CPU** sólo se puede conseguir una ilusión de hilos concurrentes de control, normalmente mediante algún algoritmo de tiempo compartido.

En esto manejamos dos tipos de procesos: **pesados** y **ligeros**.

**Proceso Pesado:** Es aquel que es comúnmente manejado de forma autónoma por el sistema operativo, este tiene su propio espacio de direcciones.

**Proceso Ligero:** Existe dentro de un solo proceso del sistema operativo en compañía de otros procesos ligeros y comparten el mismo espacio de direcciones.

Recordemos que la Programación orientada a objetos se centraliza en la abstracción de datos, encapsulamiento y herencia, mientras qué la concurrencia se centra en la abstracción de procesos y la sincronización.

Una vez que se tiene la concurrencia en un sistema, debemos de tomar en cuenta cómo los objetos activos se sincronizan con otros.

![image](https://raw.githubusercontent.com/wlizama/MDManual/master/assets/images/ejemplo-interbloqueo.png "Ejemplo interbloqueo de Procesos")

>**Como se puede observar en la imagen el proceso P1 esta solicitando el recurso R2, pero dicho recurso lo tiene asignado P2, lo mismo sucede con R1, lo está solicitando P2 pero P1 lo está utilizando.**

## ¿Qué es Persistencia?

>**Es la propiedad de un objeto por la que su existencia trasciende el tiempo es decir, el objeto continúa existiendo después de que su creador deja de existir y/o espacio.**

Dicho de otra manera, la persistencia es la acción de mantener la información del objeto de una forma permanente (guardarla), pero también debe de poder recuperarse dicha información para que pueda ser utilizada nuevamente.

La persistencia es el mecanismo que se usa para mantener información almacenada.

Para la persistencia los objetos podrían clasificarse en dos tipos **objetos transitorios** y **objetos persistentes**.

**Transitorios:** Son aquellos que su tiempo de vida depende del espacio del proceso que lo creo.

**Persistentes:** Son aquellos que su estado es almacenado en un medio temporal para su posterior reconstrucción y utilización, por lo cuál el objeto no depende del proceso que lo creo.

Un ejemplo de la persistencia es aquel objeto que se crea para luego ser guardado en la base de datos.

---

[:arrow_backward: Tipos de datos](https://github.com/wlizama/MDManual/blob/master/content/POO/6-Tipos-de-datos.md) | [:book: Indice POO](https://github.com/wlizama/MDManual/tree/master/content/POO)
--- | ---
