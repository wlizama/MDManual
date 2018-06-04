# Fundamentos de Arquitectura de Software

>_"La estructura del sistema, compuesta por elementos de software, sus propiedades visibles y sus relaciones"_

**Ley de Conway***

>_"Cualquier pieza de software refleja la estructura organizacional que la produjo.""_

## 1. El proceso de desarrollo de software

### Etapas del proceso de desarrollo de software

El proceso de desarrollo tradicional tiene etapas muy marcadas, que tienen entradas, procesos y salidas que funcionan como entradas de la siguiente etapa.

+ **Análisis de requerimientos**: Todo nace de un disparador que nos crea la necesidad de crear un artefacto o un sistema. Necesitamos entender cuál es el problema que queremos resolver. Hay requerimientos de negocio, requerimientos funcionales, requerimientos no funcionales.

    + **Requerimientos funcionales** son todos aquellos servicios o cosas que debe hacer la aplicación o sistema que se esta creando.

    + **Requerimientos no funcionales** son requerimientos que no son relacionados directamente al objeto del sistema como puede ser fiabilidad, estabilidad del sistema, capacidad de almacenamiento, tiempo de respuesta etc.

+ **Diseño de la solución**: Análisis profundo de los problemas para trabajar en conjunto y plantear posibles soluciones. El resultado de esto debe ser el detalle de la solución, a través de requerimientos, modelado, etc.

+ **Desarrollo y evolución**: Implementación de la solución, para garantizar que lo que se esta construyendo es lo que se espera. Al finalizar esta etapa tendremos un artefacto de software.

+ **Despliegue**: Aquí vamos a necesitar de infraestructura y de roles de operación para poder poner el artefacto a disponibilidad.

+ **Mantenimiento y evolución**: Desarrollo + despliegue + mantenimiento, en esta etapa estamos atentos a posible mejoras que se hacen al sistema. En esta etapa el software se mantiene hasta que el software ya deja de ser necesario.

![image](https://raw.githubusercontent.com/wlizama/MDManual/master/assets/images/proceso-de-desarrollo-software.jpg "Etapas del proceso de desarrollo de software")

### Dificultades en el desarrollo de software

En la etapa de **Diseño y Desarrollo** estamos concentrados en encontrar cuáles son los problemas que queremos resolver. Estos problemas los podemos dividir en dos grandes tipos de problemas.

**Esenciales**: Los podemos dividir en 4.

  1. **La complejidad**, cuándo lo que tenemos que resolver es complejo en si mismo. En el caso de adiciones y todas las acciones que conlleven al sistema a ser más complejo.

       _Manejo del problema de complejidad_: No desarrollar: Comprar - OSS
  
  2. **La conformidad**, en qué contexto se usa el software y cómo debe adecuarse al mismo. Se incluyen todo lo que le compete. _Ej_: Ambiente, conectividad, impuestos, etc.

       _Manejo del problema de complejidad_: Prototipado rápido, feedback y ciclos rápidos para soluciones pequeñas.
  
  3. **Tolerancia al cambio**, posibilidad del cambio en el mismo y que sea responsivo a diferentes contextos.
       
       _Manejo del problema de complejidad_: Desarrollo Evolutivo, desarrollos pequeños. Paso a paso pero de manera firme e ir haciendo crecer el software.
  
  4. **Invisibilidad**, problemas de tangibilidad nula.

       _Manejo del problema de complejidad_: Grandes diseñadores, Arquitectos que saben abtraer el problema y que realiza soluciones elegantes, de manera simple, con la mejor calidad posible en los componentes que lo necesitan.

**Accidentales**: Está relacionado con la plataforma que vamos a implementar, tecnología, lenguajes, frameworks, integraciones, etc, tienen 3 entornos:

  1. **Lenguajes de alto nivel**, son las complicaciones que surgen al lidiar con los lenguajes que se escogieron para el desarrollo del proyecto. 
  
  2. **Multi-procesamiento**, es la necesidad de resolver o atender a varios problemas en un mismo momento.
  
  3. **Entornos de programación**, son los problemas que devienen de las herramientas que hemos usado para resolver los problemas entiéndase frameworks compilados librarías etc.

> "Concidero a la especificación, diseño y comprobación del concepto la parte difícil de hacer software. (...) Si esto es cierto, hacer software siempre será difícil. No existe la bala de plata."
>
> Del libro _No Silver Bullet_ (Frederick P. Brooks Jr., 1986)

### Roles

Es importante que diferenciemos el ROL del puesto de trabajo, hay roles que pueden ser desarrollados por la misma persona.

**Experto del dominio (stakeholders)** En una metodologia tradicional, es la persona a la que acudimos para entender las necesidades del negocio. En metodologias Agiles.

**Analista** funcional/de negocio, la persona responsable de definir los requerimientos que van a llevar al software a u buen puerto. En el caso de Agiles el dueño del producto es quien arma las historias y que nos acompaña en el proceso de construcción del software.

**Administrador de sistemas / DevOps** Es el rol de operaciones y desarrollo, son las personas responsables de la infraestructura que alojara nuestra aplicación.

**Equipo de desarrollo**  QA / Testing se encargan de la evaluación de nuestro software, comprobar que lo que se esta haciendo es lo que se espera que se haga. Desarrolladores involucrados en la construcción del software. Arquitecto, diseña la solución y analisis de los requerimientos, es un papel mas estrategico. La arquitectura emerja del trabajo de un equipo bien gestionado.

**Gestor del proyecto / facilitador** Llevan al equipo a través del proceso iterativo e incremental, entender lo que pasa con el equipo y motivar el avance en el desarrollo del producto.

## 2. Introducción a la arquitectura de software

### Objetivos del arquitecto

Cada uno de los stakeholder tiene que ser conectado por el Arquitecto con sus requerimientos.

**Stakeholder -> Arquitecto -> Requerimientos = Implementaciónes en el Sistema.**

Los Requerimientos de cada stakeholder afectan de forma única el sistema.

**Cliente**: Entrega a tiempo y dentro del presupuesto.

**Manager**: Permite equipos independientes y comunicación clara.

**Dev**: Que sea fácil de implementar y de mantener.

**Usuario**: Es confiable y estará disponible cuando lo necesite.

**QA**: Es fácil de comprobar.

La unión de todos estos requerimientos (funcionales o no funcionales) van a llevar al arquitecto a tomar decisiones que impacten sobre el sistema.