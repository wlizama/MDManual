# Fundamentos de Arquitectura de Software

>_"La estructura del sistema, compuesta por elementos de software, sus propiedades visibles y sus relaciones"_

**Ley de Conway**

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

**Experto del dominio (stakeholders)** en una metodologia tradicional, es la persona a la que acudimos para entender las necesidades del negocio. En metodologias Agiles.

**Analista** funcional/de negocio, la persona responsable de definir los requerimientos que van a llevar al software a u buen puerto. En el caso de Agiles el dueño del producto es quien arma las historias y que nos acompaña en el proceso de construcción del software.

**Administrador de sistemas / DevOps** es el rol de operaciones y desarrollo, son las personas responsables de la infraestructura que alojara nuestra aplicación.

**Equipo de desarrollo QA / Testing** se encargan de la evaluación de nuestro software, comprobar que lo que se esta haciendo es lo que se espera que se haga. Desarrolladores involucrados en la construcción del software. Arquitecto, diseña la solución y analisis de los requerimientos, es un papel mas estrategico. La arquitectura emerja del trabajo de un equipo bien gestionado.

**Gestor del proyecto / facilitador** llevan al equipo a través del proceso iterativo e incremental, entender lo que pasa con el equipo y motivar el avance en el desarrollo del producto.

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

## 3. Análisis de requerimientos

### Entender el problema

**El espacio del problema**

Detalla que es lo que se va a resolver sin entrar en detalles del "cómo".

**El espacio de la solución**

Brinda el detalle del "cómo", reflejando los detalles del problema detectado, evitando resolver problemas que no se quiere resolver.

### Requerimientos

Una vez que entendemos el espacio del problema y el espacio de la solución, vamos a entrar a analizar los requerimientos de nuestro sistema.

**Requerimientos de producto:**

Los podemos dividir en 3

- Capa de requerimientos de negocio, son reglas del negocio que alimentan los requerimientos del negocio.

- Capa de usuario, tienen que ver en cómo el usuario se desenvuelve usando el sistema, qué atributos del sistema se deben poner por encima de otros.

- Capa Funcional, se ven alimentados por requerimientos del sistema, ¿qué cosas tienen que pasar operativamente?

- Esta capa se ve afectada por las restricciones que pueden afectar operativamente a lo funcional.

**Requerimientos de proyecto:**

Tienen que ver más con el rol de gestor de proyectos, se usan para dar prioridad a los requerimientos del producto. Estos dos mundos de requerimientos hablan de las prioridades del equipo de trabajo del proyecto.

**Requerimientos de producto:**

  + **Requerimientos funcionales**: Tienen que ver con las historias de usuarios, que hablan sobre específicamente lo que hace el sistema, por ejemplo que usuario ingrese al sistema.

  + **Requerimientos no funcionales**: son aquellos que agregan cualidades al sistema, por ejemplo que el ingreso de ese usuario sea de manera segura.

### Riesgos

Los riesgos son importantes para priorizarlos y atacarlos en orden y asegurar que las soluciones arquitectónicas que propongamos resuelvan los problemas más importantes.

Intenta tratar los riesgos con posibles escenarios de fracaso y que pasaría en caso de que ese riesgo se haga real.

**Identificación de los riesgos:**

+ **Toma de Requerimientos (Requerimientos funcionales)**: Se calificará su riesgo de acuerdo a su dificultad o complejidad.

+ **Atributos de calidad (Requerimientos NO funcionales)**: Se calificará su riesgo de acuerdo a la incertidumbre que genere, cuanto mas incertidumbre hay, mas alto es el riesgo.

+ **Conocimiento del dominio**: Riesgo prototípico, son aquellos que podemos atacar de forma estándar.

Una vez que tenemos los riesgos identificados, debemos priorizarlos, recuerda que no es necesario mitigarlos todos, debemos siempre tener en cuenta y dar prioridad a aquellos riesgos que ponen en peligro la solución que se esta construyendo.

### Restricciones

Las restricciones en el contexto de un proceso de desarrollo de software se refiere a las restricciones que limitan las opciones de diseño o implementaciones disponibles al desarrollar.

Los _StakeHolders_, nos pueden poner limitaciones relacionadas con su contexto de negocio, ejemplo:

+ **Limitaciones legales** la implementación de un producto podría tener restricciones en algún país, y esto seria una limitante a considerar para el desarrollo del producto.

+ **Limitaciones técnicas** relacionadas con integraciones con otros sistemas.

+ **El ciclo de vida del producto** agregará limitaciones al producto, por ejemplo a medida que avanza el proceso de implementación el modelo de datos va a ser más difícil de modificar.

**Nota:**

_El arquitecto debe balancear entre los requerimiento y las restricciones._

## 4. Estilos de arquitectura

### Estilos: Llamado y retorno

Cada uno de los componentes hacen invocaciones a los componentes externos y estos retornan información. Cada componente hace un llamado y espera una respuesta.

**Programa y subrutinas** Instrucciones secuenciales que el programa ejecutaba una por una. Luego se hacian instrucciones de salto, de aqui surgieron las funciones que son bloques de codigo que podemos invocar en cualquier momento.

**Orientado a objetos** la abstracción es mayor en comparación con el paradigma anterior, se usa para aplicaciones que ya sabemos que vamos a usar durante mucho tiempo. La abstracción ya no es la subrutina, ahora tenemos objetos que se hacen llamados entre si y esperan respuestas.

### Estilos: Flujo en datos

Se basa en un patrón tuberías y filtros. Este consta de un conjunto de componentes denominados _"filtros"_, conectados entre sí por _"tuberías"_, que transmiten los datos desde un componente al siguiente. Cada filtro trabaja de manera independiente de los componentes que se encuentren situados antes o después de el.

### Estilos: Centradas en datos

**Estilo de pizarrón** permite centralizar los datos en una sola base de datos, alimentada por varias partes involucradas, una vez que todas las partes interesadas ingresan los datos, el sistema centralizado genera una salida.

**Estilo Centralizado** en este caso el sistema posee los datos centralizados en una base de datos, y hay dos (02) sistemas que comparten la misma base de datos.

**Estilo Experto** en este caso el sistema que centraliza los datos, tiene la capacidad de entender los datos y consultas que realiza el cliente, generando salidas inteligentes. (inteligencia artificial).

### Estilos: Componentes independientes

**Invocación implícita**: Suele ser basada en eventos, habla de como hacer para que nuestras aplicaciones se manden mensajes entre si. Cuando se tiene eventos, naturalmente se tienen componentes y un bus de eventos donde los componentes van a publicar eventos y luego el bus de eventos los va a notificar. Aquí se encuentra **Publicar** y **Suscribir** que trata de un componente que publica y otro componente que suscribe, todo a través del bus de eventos. También existe el **Enterprise Service Bus** tiene componentes registrados los cuales se pueden comunicar con el bus, los componentes no se conocen entre si, pero están programados para cumplir con su objetivo.

**Invocación explícita**: Tiene que ver con el desarrollo de componentes que si se conocen entre si, pero que sean desarrollado independientemente. Aquí se encuentra Orientado al Servicio en donde todos los componentes se registran al _"Registro central"_ y después indican donde comunicarse.

**ARQUITECTURA ORIENTADAS A SERVICIOS**:

El _Enterprise Services Busses_, sabe que proceso tiene que llevar a cabo para lograr su cometido, dando a los componentes la información que éstos requieran. El ESB, es inteligente.

Es necesario tener en cuenta que cualquier actualización del sistema, mantiene conectado a los componentes que brindan servicios de consulta.