# Encapsulamiento

Definamos Encapsulamiento:

>**Es el proceso de almacenar en una misma sección los elementos de una abstracción que constituyen su estructura y su comportamiento; sirve para separar el interfaz contractual de una abstracción y su implantación.**

Pero..! _¿Cómo consigo esto?_, ¡tranquilo! esto se consigue a través de la ocultación de información, ves como todo es más fácil estando relajado, _¿No sabes que es la ocultación de información?_, _¡Tranquilo!, No, aún no estás tranquilo, ¿Ya?_ seguimos, Ocultación de información es el proceso de ocultar “Todos los Secretos” de un objeto que no aportan a sus características específicas.

Para que la abstracción funcione como debe, la implementación debe estar encapsulada,  nunca está de más recordar que cada clase debe tener dos partes, una interfaz y una implementación, tranquilo no te asustes si no sabes que es una clase, ya llegaremos a ese tema, de momento manténgase concentrado en la encapsulación.

##Existen tres niveles de acceso para el encapsulamiento, los cuales son:

**Público (Public):** Todos pueden acceder a los datos o métodos de una clase que se definen con este nivel, este es el nivel más bajo, esto es lo que tu quieres que la parte externa vea.

**Protegido (Protected):** Podemos decir que estás no son de acceso público, solamente son accesibles dentro de su clase y por subclases.

**Privado (Private):** En este nivel se puede declarar miembros accesibles sólo para la propia clase.

_**Ejemplo:**_

**Contexto 1:  Se necesita que cualquiera pueda acceder a el color de un vehículo, entonces:**

**Opción a:** Declaro entonces COLOR como Privado

**Opción b:** Declaro entonces COLOR como Protegido

**Opción c:** Declaro entonces COLOR Como Público

_Correcta Opción b_

**Contexto 2: Se necesita qué  color se pueda acceder a través no sólo de vehículo, sí no ahora también de Buses,  y como todos sabemos un bus es un tipo de vehículo, entonces también deberá tener acceso a color.**

**Opción a:** Declaro entonces COLOR como Privado

**Opción b:** Declaro entonces COLOR como Protegido

**Opción c:** Declaro entonces COLOR Como Público

_Correcta Opción b_

**Contexto 3: Se necesita que color se pueda acceder solamente para vehículo.**

**Opción a:** Declaro entonces COLOR como Privado

**Opción b:** Declaro entonces COLOR como Protegido

**Opción c:** Declaro entonces COLOR Como Público

_Correcta Opción a_

---

[:arrow_backward: Abstracción](https://github.com/wlizama/MDManual/blob/master/content/POO/2-Abstraccion.md) | [:book: Indice POO](https://github.com/wlizama/MDManual/tree/master/content/POO) | [Modularidad :arrow_forward:](https://github.com/wlizama/MDManual/blob/master/content/POO/4-Modularidad.md)
|--- | --- | --- |