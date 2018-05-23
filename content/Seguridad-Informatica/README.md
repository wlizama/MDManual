# Seguridad Informática

Una definición simple seria el proceso de prevenir y detectar el uso no autorizado de un sistema informático. Implica el proceso de proteger contra intrusos el uso de nuestros recursos informáticos con intenciones maliciosas o con intención de obtener ganancias, o incluso la posibilidad de acceder a ellos por accidente.

## Introducción al Pentesting

Accion de acceder mediante técnicas de Hacking a sistemas de información, electronicos o físicos. Se incluyen ataques de ingenieria social y seguridad física con conocimientos de cerrajeria y seguridad física electrónica y de monitoreo en video.

El **Ethical Hacking** tiene cinco fases:


- Reconocimiento

- Escaneo

- Explotacion (Conseguir acceso)

- Mantener el acceso

- Eliminar las huellas

### Fase de reconocimiento:

Obtención de la mayor cantidad de información del objetivo

+ Redes Wifi y la seguridad que tienen, fabricante del router, versión de firmware, sistema operativo

+ Información del hardware de sus servidores web

+ Ubicación de los servidores web

+ Tecnología que utilizan para el desarrollo de sus herramientas web

+ Nombre de la persona que administra el servidor web

+ Nombre de las personas que trabajan en la compañia

+ Detalles de los proveedores de la compañia y nombre de las personas que trabajan para los proveedores

+ Detalles de los servicios subcontratados por la compania objetivo

+ Información de la empresa objetivo, números de teléfono, personas que trabajan, gerentes, dueños, personas que conforman la junta directiva, horarios del personal, turnos en los que se trabaja

+ Malas prácticas de PI de la empresa objetivo. Verificación de politicas de compliance.

+ Aplicacion de tecnicas [OSINT](https://en.wikipedia.org/wiki/Open-source_intelligence)

### Fase de escaneo

+ En esta fase se realizan operaciones mas activas, como aplicacion de OSINT por sobre los servidores web del objetivo

+ Escaneo de puertos

+ Escaneo de servicios

+ Obtención de versiones de firmware y software

+ Detalles de los manufacturers

+ Sistema operativo funcionando en los servidores web

+ Puertos abiertos en el servidor

+ Servicios que corren en el servidor web, sus versiones de software y detalles de vulnerabilidades.

+ IPs de la red

+ Dominios

+ Subdominios

+ Servicios corriendo dentro de la red

+ Crear un modelo de escaneo tanto interno como externo

### Explotacion

Identificacion de las fallas que tienen esos servicios. Esto implica la obtencion de una base de datos de vulnerabilidades. Revisar Metasploit.

### Mantener el acceso

APT’s: Advance Persistent Threats. (Consiste en la aplicacion de backdoors modificando los sistemas host de manera que sea imposible detectarla. Es posible activar servicios legitimos o alterar elementos del entorno operativo del host para crear estas puertas traseras)

### Borrar las huellas

Este punto es uno de los más importantes, ya que es el proceso que se realiza para eliminar cualquier rastro que comprometa al atacante.

## Metodologias de pentesting

**Caja negra** implica todas las fases del pentesting

**Caja Blanca** Se tiene toda la información de las dos primeras fases, provista por el contractor que busca desarrollar el pentesting.

**Caja Gris** se conoce parcialmente la información del contractor.

## Vectores de ataque

**APT (Advance Persistent Threat)** Este tipo de ataques es uno de mayor gravedad a los habituales, este posee características que hacen que sus efectos dañinos sean más fuertes. El atacante que usa este tipo de vector de ataque es muy paciente, mucho más que el atacante promedio.

**Botnets** En este tipo de ataque se usan virus troyanos especiales para violar la seguridad de las computadoras de varios usuarios, así de esta forma tomar el control de cada una de ellas y organizarlas en una red de manera que el atacante pueda administrarlas de forma remota. La palabra Botnet se forma a partir de las palabras **“robot”** y **“red”**.

**Ataques internos** Este tipo de ataque son los más comunes (aproximadamente el 80%) y son los que más impacto pueden generar en una infraestructura ya que por estar en el interior se es más fácil acceder a la red interna y desde allí atacar.

**Amenazas mobiles** Este tipo de ataque parte de la tendencia de llevar consigo un dispositivo móvil y por medio de ellos acceder a la información, a la red de una empresa.


## Terminos importantes

**¿Que es un activo?** Todo aquel elemento electrónico o no que puede tener incidencia sobre la seguridad de la información del objetivo.

**¿Que es una amenaza?** Todo aquel factor que puede tener incidencia en la estabilidad o privacidad de la informacion para el objetivo.

**¿Que es una vulnerabilidad?** Una vulnerabilidad es toda debilidad, carencia, falla o procedimiento que pueda generar una amenaza.

**¿Que es un riesgo?** Es un proceso que comprende la identificación de las vulnerabilidades y amenazas dando lugar a un ataque.

**¿Que es un exploit?** Es la implementación de una vulnerabilidad para afectar al objetivo.

**¿Que es el Payload?** Es la ejecución que se realiza dentro del sistema una vez aplicado el exploit.

_Proceso: Se detecta la vulnerabilidad, se ejecuta el exploit y posteriormente se implementa el payload._