# Redes de Internet

Según [Andrew S. Tanenbaum](https://es.wikipedia.org/wiki/Andrew_S._Tanenbaum)

> Una red de computadoras es un conjunto de equipos informáticos y software conectados entre sí por medio de dispositivos físicos o inalámbricos que envían y reciben impulsos eléctricos, ondas electromagnéticas o cualquier otro medio para el transporte de datos, con la finalidad de compartir información, recursos y ofrecer servicios.

## Qué es la red, Internet, LAN, WAN y Topologías de Red

El objetivo de una red es transportar un elemento de un lugar a otro.

Siempre tenemos un punto de partida y un punto de llegada.

Una red informática es un conjunto de equipos conectados entre sí por medio de dispositivos físicos o inalámbricos que envían y reciben impulsos eléctricos, ondas electromagnéticas, o cualquier otro medio para el transporte de datos.

**LAN (Local Area Network-Red de area local):** Es una red que conecta ordenadores o dispositivos en un área relativamente pequeña con el fin de compartir recursos, datos o apps.

**WAN (Wide Area Network-Red de area amplia):** Este tipo de red generalmente sirve para conectar dispositivos que se encuentran separados por un área geográfica extensa, es decir, si las redes _LAN_ conectan computadores o dispositivos en un area "pequeña", las redes _WAN_ conectaran “sucursales” con sedes centrales. 

**MAN (Metropolitan Area Network-Red de área metropoltana):** Es una infraestructura de red que abarca un area mayor a una LAN pero menor que una WAN.

_ISP (Internet Service Provider-Proveedor de servicios de Internet):_ Es la empresa que te brinda la conexión a Internet y te permite navegar por la red. 

**Internet:** Es una red de redes interconectadas mundialmente.

**Topología de red:** Es el mapa físico y lógico de la red.

## Intranet y Extranet

Son dos formas en las que podemos diseñar e implementar las redes de acuerdo con caraterísticas de acceso que queremos dar a los usuarios.

### Intranet

Son aquellas redes internas que en las que el acceso a la información esta estrictamente limitada a personal de la compañía. Este tipo de redes se restringen con el uso de software y se usan en situaciones en las que la información a la que pueden acceder los usuarios es confidencial.

### Extranet

El siguiente nivel de acceso sucede cuando las compañías requieren dar acceso seguro y bajo confidencialidad a usuarios externos incluso a organizaciones diferentes a la que posee la información.

Esto puede pasar por ejemplo cuando una compañía requiere compartir documentos o información con proveedores o contratistas.

## Topologías de Red

La topología de red nos permite identificar la forma en que los nodos están conectados y la información se envía a través de los medios y de los nodos para viajar de un lugar a otro.

### Tipos de Topologías

#### Topología punto a punto

Se aprecia cuando tenemos dos nodos conectados por un medio para enviar información, un punto envía información al otro.

**Ventajas**

+ Fáciles de configurar.

+ Menor complejidad.

+ Menor costo dado que no se necesita dispositivos de red ni servidores dedicados.

**Desventajas**

+ Administración no centralizada.

+ No son muy seguras.

+ Todos los dispositivos pueden actuar como cliente y como servidor, lo que puede ralentizar su funcionamiento.

+ No son escalables

+ Reducen su rendimiento

![image](https://upload.wikimedia.org/wikipedia/commons/a/a8/Red_punto_a_punto.png "Topología punto a punto")

### Topología de bus

Una red en bus es aquella topología que se caracteriza por tener un único canal de comunicaciones (denominado bus, troncal o backbone) al cual se conectan los diferentes dispositivos. De esta forma todos los dispositivos comparten el mismo canal para comunicarse entre sí.

**Ventajas**

+ Facilidad de implementación y crecimiento.

+ Fácil adaptación.

+ Simplicidad en la arquitectura.

+ Es una red que no ocupa mucho espacio.

**Desventajas**

+ Hay un límite de equipos dependiendo de la calidad de la señal.

+ Puede producirse degradación de la señal.

+ Complejidad de reconfiguración y aislamiento de fallos.

+ Limitación de las longitudes físicas del canal.

+ Un problema en el canal usualmente degrada toda la red.

+ El desempeño se disminuye a medida que la red crece.

+ El canal requiere ser correctamente cerrado (caminos cerrados).

+ Altas pérdidas en la transmisión debido a colisiones entre mensajes.

![image](https://upload.wikimedia.org/wikipedia/commons/d/dd/Topologia_magistrali.svg "Topología de bus")

### Topología de anillo

Este tipo de topología consiste en que cada nodo tiene una única conexión de entrada y una conexión de salida. Un token de confirmación viaja a través de cada nodo avisando que se envió y fue recibida correctamente.

Este tipo de topología aunque garantiza el envío de la información puede llegar a ser un poco lenta ya que ésta debe pasar por cada nodo intermedio antes de alcanzar su objetivo. En el caso de que uno de los nodos fallé esto puede afectar el funcionamiento de la red.

**Ventajas**

+ El sistema provee un acceso equitativo para todas las computadoras.

+ El rendimiento no decae cuando muchos usuarios utilizan la red.

+ Arquitectura muy sólida.

+ Sistema operativo caracterizado con un único canal

**Desventajas**

+ Longitudes de canales (si una estación desea enviar a otra, los datos tendrán que pasar por todas las estaciones intermedias antes de alcanzar la estación de destino).

+ El canal usualmente se degradará a medida que la red crece.

+ Difícil de diagnosticar y reparar los problemas.

+ Si se encuentra enviando un archivo podrá ser visto por las estaciones intermedias antes de alcanzar la estación de destino.

+ La transmisión de datos es más lenta que en las otras topologías (Estrella, Malla, Bus, etc), ya que la información debe pasar por todas las estaciones intermedias antes de llegar al destino.

![image](https://upload.wikimedia.org/wikipedia/commons/7/71/Netzwerktopologie_Ring.png "Topología de anillo")

### Topología de estrella

En esta topología todos los nodos están conectados a un punto central, esta implementación permite garantizar el funcionamiento de la red, de forma que si alguno de los nodos falla esto no va a afectar para nada el funcionamiento ni el rendimiento de la red.

Esta topología se usa mucho en redes _LAN_ por ejemplo de oficinas en las que hay un switch al que llegan todas las conexiones de los dispositivos a través de cable.

Es una topología que permite agregar nodos nuevos siempre que el dispositivo central lo permita, sin embargo en caso de que el nodo central falle toda la red dejará de funcionar.

**Ventajas**

+ Posee un sistema que permite agregar nuevos equipos fácilmente.

+ Reconfiguración rápida.

+ Fácil de prevenir daños y/o conflictos, ya que no afecta a los demás equipos si ocurre algún fallo.

+ Centralización de la red.

+ Fácil de encontrar fallas

**Desventajas**

+ Si el hub (repetidor) o switch central falla, toda la red deja de transmitir.

+ Es costosa, ya que requiere más cables que las topologías en bus o anillo.

+ El cable viaja por separado del concentrador a cada computadora.

![image](https://upload.wikimedia.org/wikipedia/commons/5/53/Netzwerktopologie_Stern.png "Topología de estrella")

### Topología de malla

En las topologías de tipo malla todos los nodos están conectados entre sí, este tipo de conexión permite que cada nodo pueda actuar como servidor y como cliente, esta es una forma óptima de mantener la conexión entre dispositivos en una red ya que se reduce a uno cantidad de dispositivos por los que debe viajar la información de un dispositivo a otro y en caso de que un nodo de la red falle los datos pueden ser enviados por otro camino lo que asegura disponibilidad.

**Ventajas**

+ Es posible llevar los mensajes de un nodo a otro por diferentes caminos.

+ No puede existir absolutamente ninguna interrupción en las comunicaciones.

+ Cada servidor tiene sus propias comunicaciones con todos los demás servidores.

+ Si falla un cable el otro se hará cargo del trafico.

+ No requiere un nodo o servidor central lo que reduce el mantenimiento.

+ Si un nodo desaparece o falla no afecta en absoluto a los demás nodos.

**Desventajas**

+ Es costosa de instalar ya que requiere de mucho cable.

![image](https://upload.wikimedia.org/wikipedia/commons/9/91/Netzwerktopologie_vermascht.png "Topología de malla")

### Topología de árbol

En esta topología contamos con varios dispositivos intermedios que permiten que otros nodos se conecten. Por ejemplo podemos tener un punto inicial que recibe la conexión a Internet desde el ISP, de allí viaja por el medio a un switch que distribuye a otros dispositivos que pueden ser nodos u otros dispositivos intermedios, switches, routers etc quienes a su vez envían los datos a otros dispositivos iguales.

**Ventajas**

+ Cableado punto a punto para segmentos individuales.

+ Soportado por multitud de vendedores de software y de hardware.

+ Facilidad de resolución de problemas.

**Desventajas**

+ Se requiere mucho cable.

+ La medida de cada segmento viene determinada por el tipo de cable utilizado.

+ Si se cae el segmento principal todo el segmento también cae.

+ Es más difícil su configuración.

+ Si se llegara a desconectar un nodo, todos los que están conectados a él se desconectan también.

![image](https://upload.wikimedia.org/wikipedia/commons/a/ad/Netzwerktopologie_Baum.PNG "Topología de árbol")


## Banda ancha y velocidad de internet

Teniendo en cuenta que un bit puede ser un 0 o un 1 tenemos que:

**1 Kilobit (Kb-Kbit)** = 1000 bits **(b)**

**1 Megabit (Mb)** = 1000 Kilobits **(Kb)**

**1 Byte (B)** = 8 bits **(b)** => Al byte también lo llaman octeto

**1 Kilobyte (KB)** = 1024 Bytes **(B)**

**1 Megabyte (MB)** = 1024 Kilobytes **(KB)**

Ejemplo de calculo de velocidad

```
  Mi velocidad a : 20 Mbps

  De Mb -> B

  20 Mb = 2 500 000 B

  De B a KB

  2 500 000 B = 2441.41 KB

  De KB a MB

  2441.41 KB = 2.44141 MB

  Velocidad en MB = 2.44
```

## La Red Covergente

Como su palabra lo indica convergen, en la que podemos trasmitir tanto la voz, los datos y video, por el mismo medio y ser utilizadas consecutivamente sin necesidad de una infraestructura para cada una de ellas, como era antes, además del menor coste de mantenimiento de las infraestructura.

Podemos poner como ejemplo las líneas ADSL, en las cuales conviven los tres servicios conjuntamente, por las cuales se transmite la voz por el medio de cobre, con el que convive la transmisión de datos, por los que además se transmiten los servicios de TV, como puede ser la televisión bajo demanda o streaming.

Eso es lo que podemos decir que es una red convergente. La interacción de varios servicios de comunicación por un solo medio.

## Métodos de acceso a los dispositivos

### Protocolo Telnet

Acrónimo de _"Telecommunication Network"_, es un protocolo de red que permite comunicarse en modo texto con otra máquina de manera que podamos controlarla de forma remota. Este protocolo se basa en la arquitectura **cliente-servidor**, donde el servidor será el ordenador que vamos a manejar y el cliente el ordenador desde el que vamos a controlar el servidor.

Este es un protocolo muy simple, sin embargo, cuenta con grave problema de seguridad, y es que las conexiones no son seguras, y el tráfico viaja sin cifrar.

### SSH

_SSH o Secure Shell_, es un protocolo de administración remota que permite a los usuarios controlar y modificar sus servidores remotos a través de Internet. El servicio se creó como un reemplazo seguro para el Telnet sin cifrar y utiliza técnicas criptográficas para garantizar que todas las comunicaciones hacia y desde el servidor remoto sucedan de manera encriptada. Proporciona un mecanismo para autenticar un usuario remoto, transferir entradas desde el cliente al host y retransmitir la salida de vuelta al cliente.

Cualquier usuario de **Linux** o **macOS** puede hacer SSH en su servidor remoto directamente desde la ventana del terminal. Los usuarios de **Windows** pueden aprovechar los clientes SSH como Putty. Puede ejecutar comandos shell de la misma manera que lo haría si estuviera operando físicamente el equipo remoto.

Por defecto SSH usa el puerto 22 y Telnet utiliza el puerto 23, una medida básica de seguridad es configurarlos en otros puertos que no sean los establecidos por defecto.

## Aspectos básicos de comunicación

Los elementos básicos de la comunicación son: El emisor, el mensaje, el canal o el medio y el receptor. Los protocolos son las normas que nos indican establecer una comunicación que sea efectiva. Necesitamos establecer protocolos que nos ayuden a ver que la información pasen por todas las capas que tiene los procesos de comunicación.

Los protocolos determinan las siguientes características:

+ Codificación del mensaje

+ Formato y encapsulamiento del mensaje

+ Tamaño del mensaje

+ Sincronización

+ Opciones de entrega

El formato y la estructura del mensaje, la información que queremos transmitir debe tener una forma para que pueda ser enviada por el medio que queremos enviarlo.

**Tamaño del mensaje:** Las señales muy grandes no son transmitidos, son rechazados. El tamaño es importante y se es limitado.

**Sincronización:** Contamos con protocolos que nos ayudan a determinar cuando se esta enviando un mensaje, que ya llego un mensaje, que se puede llegar otro.

**Opción de entrega:** Unicast se le envía a un solo host, Multicast permite enviar a un grupo más pequeño, no a todos los host, Broadcasting nos envía paquetes a toda la red.

## Modelos de referencia Modelo OSI, modelo TCP/IP

Los modelos de protocolos de referencia son normas y estándares que nos ayudan a determinar las fases y los protocolos por los que la información va a viajar hasta llegar a su destino.

### Capas de Modelo de referencia OSI

**Física**: Es la capa de los medios, son los cables, elementos que transmiten la información que transportan las señales y que llevan los mensajes

**Enlace de datos**: Los equipos que hacen los direccionamiento. Estamos hablando de los medios fiscos pero no del cableado sino de los dispositivos que nos permiten codificar y decodificar la información.

**Red**: es la capa que hace el direccionamiento lógico, el direccionamiento de IP.

**Transporte**: Nos da la conexión de extremo a extremo. Tiene los protocolos TCP y UDP. Nos aseguran que el mensaje fue enviado y recibido.

**Sesión**: Es una capa que se abre y nos mantiene el flujo de información que nos permite la comunicación entre los dispositivos de red.

**Presentación**: Se refiere a la representación que tiene los archivos desde las aplicaciones.

**Aplicación**: es la capa que tu ves, la que ves como usuario final

## Segmentación de los mensajes y Unidades de Datos de Protocolo PDU

Dos características que nos ayudan son el tamaño del mensaje y el formato del mensaje.

+ La segmentación consisten en tomar un mensaje muy grande y dividirlo en mensajes más pequeños.

+ La multiplexación es la combinación de dos o más canales de información en un solo medio de transición.

**PDU Protocol Data Unit** es una unidad que nos permite identificar la información a medida que es transmitida a través de las capas de red.

## Capa Física y Medios de Red

Hay algunas organizaciones que regulan los estándares de la capa física como **TIA** y la **EIA**.

La capacidad de los medios para transportar los datos depende del ancho de banda, el rendimiento y la capacidad de transferencia útil.

### Funciones de la capa física

Controlar los componentes físicos, codificar y decodificar los datos, señalizar, convertir esos datos en señales que puedan ser enviados por los medios.

La capa física está compuesta por:


+ **Cable de cobre**: Lleva impulsos eléctricos.

+ **Cable de fibra óptica**: Lleva impulsos de luz, emite 1 y 0 en forma de luz. No suele tener interferencia.

+ **Inalámbrico (ondas de radio)**: Viaja por Ondas Electromagnéticas.

## Capa de enlace de datos

Es la que se encarga de comunicar la parte física con la parte logica.

**MAC**: Capa de acceso al medio fisico. Esto es una direccion que identifica unicamente a cada una de las tarjeta de red que tiene nuestros dispositivos.

**LLC**: Capa de acceso lógico, esta capa es la que nos permite pasar los datos de forma lógica, transformarlos para que la capa de red pueda recbirla.

**Gestion del canal**: la capa va a contar con protocolos que le permiten a la señal decir si va a una solo canal o si es duplex o full duplex.

**Segmentación de la trama**: El tamaño del mensaje no puede ser muy grande ni muy pequeño. Verifica que no sean tramas muy largas ni cortas.

**Control de errores y recuperación de fallos**: Lo que hace es poner caracteres que nos ayudan al final de la trama para identificar si esos datos llegaron completos, si se agregó información por el camino o si se perdió.

## Diferencias entre Switch y el Access Point

Recordemos de la capa Física y de medios de red es la que se encarga de hacer conexión entre dispositivos usando interfaces y direcciones físicas.

En esta capa contamos con varios dispositivos y vamos a ver cuáles son y sus diferencias.

### El Switch

Es el dispositivo que nos permite realizar conexiones físicas entre hosts, el switch se encarga de filtrar y direccionar los paquetes a través de la red de área local LAN.

El switch permite la conexión entre dispositivos a través del medio cableado.

Existe otros dispositivo que nos permite hacer la conexión de manera casi igual, es el **Hub**, incluso pueden verse iguales, pero no se recomienda usar este dispositivo.

Mientras el switch toma los paquetes que llegan y analiza las direcciones físicas de los hosts conectados para reenviar el paquete únicamente a su destinatario el **Hub** envía el mensaje por todos los canales, sin tener en cuenta el direccionamiento.

### Accesss Point

Otro dispositivo de la capa física es el Access Point, este dispositivo es el encargado de realizar el enlace entre las redes cableadas y las redes inalámbricas. Nos permite crear redes LAN haciendo haciendo uso de las ondas de radio.

## Capa de RED

El nivel de red o capa de red, según la normalización OSI, es un nivel o capa que proporciona conectividad y selección de ruta entre dos sistemas de hosts que pueden estar ubicados en redes geográficamente distintas. Es el tercer nivel del modelo OSI y su misión es conseguir que los datos lleguen desde el origen al destino aunque no tengan conexión directa. Ofrece servicios al nivel superior (nivel de transporte) y se apoya en el nivel de enlace, es decir, utiliza sus funciones.

Para la consecución de su tarea, puede asignar direcciones de red únicas, interconectar subredes distintas, encaminar paquetes, utilizar un control de congestión y control de errores.

Sus funciones principales son:

+ Hacer el direccionamiento de paquetes se refiere a asignar las direcciones lógicas de los paquetes.

+ Encapsulamiento de los paquetes.

+ Enrutamiento: Encontrar el camino que conecte una red con otra.

+ Desencapsulamiento de los paquetes.

## Direcciones IP

Es un identificador lógico de las interfaces de red de los dispositivos que utilizan protocolo IP para la comunicación.

### Clases de IPv4

**Clase A**

+ El primer octeto identifica la red.

+ Tres últimos octetos (24 bits) pueden ser asignados a los hots.

+ Cantidad máxima de hosts es ``2^24 - 2``

+ 16 777 214 hosts

**Clase B**

+ Dos primeros octetos para identificar la red.

+ Dos octetos finales (16 bits) para que sean asignados a los hosts.

+ Cantidad máxima de hosts por cada read es ``2^16 - 2``

+ 65 534 hosts

**Clase C**

+ Tres primeros octetos para identificar la red.

+ Octeto final (8 bits) para que sea asignado a los hosts.

+ Cantidad máxima de hosts por cada red es ``2^8 - 2``

+ 254 hosts

### IPs Públicas y Privadas

En las redes de área local se asignan direcciones a los dispositivos que permiten la conexión entre ellos. Las direcciones privadas son aquellas que no se pueden enrutar a través de Internet.

Las direcciones IP públicas sin aquellas que permiten la conexión a Internet.

Todos los dispositivos que están atrás de un mismo router tienen diferentes direcciones IP privadas únicas en ese segmento de red y una dirección pública que permite la conexión entre diferentes redes al rededor del mundo, esta dirección ip pública es la dirección del router.

El segmento de direcciones privadas se encuentra entre

10.0.0.0/8 a 10.255.255.255 para redes con conexión inalámbrica y

192.168.0.0/16 a 192.168.255.255 para redes conectadas por medio cableado

### Direcciones IP con una función o proposito

1. Direcciones privadas: no se pueden enrutar a través de internet.
  
   a. 10.0.0.0/8 a 10.255.255.255

   b. 172.16.0.0/16 a 172.31.255.255

   c. 192.168.0.0/24 a 192.168.255.255

2. Direcciones de loopback
   
   127.0.0.0/8 a 127.255.255.254

3. Direcciones de link local

   168.254.0.0/16 169.254.255.254

4. Test

   192.0.2.0/24

## Máscara de subred

Nos permite identificar a simple vista la porción de la dirección IP que se a ha asignado a la identificación de la red y la porción que se ha asignado a los hosts.

**A** - 255.0.0.0     ó 11111111.00000000.00000000.00000000

**B** - 255.255.0.0   ó 11111111.11111111.00000000.00000000

**C** - 255.255.255.0 ó 11111111.11111111.11111111.00000000

## Capa de Transporte

Es la que se encarga de definir como van a ser enviados los mensajes, de acordar o asignar puertos y establecer esos protocolos que nos van a ayudar a que el mensaje sea enviado o garantizar del envio del mensaje.

### Tareas de la Capa de Transporte

+ Segmentar los datos.

+ Realizar el seguimiento de las conversaciones individuales.

+ Identificar las aplicaciones de acuerdo al puerto.

### Protocolos TCP y UDP

**TCP** (Transmission Control Protocol) proporciona un servicio orientado a conexión y fiable.

**UDP** (_User Datagram Protocol_) proporciona un servicio no orientado a conexión y no fiable, esto quiere decir que se va a intentar por todos los medios que los datos lleguen, pero no lo garantiza.

_¿Cómo se envían los datos por la red?_ Se envían mediante **TCP** y **UDP**.

_¿Es fiable la transmisión de los datos?_ Con **TCP** sí ya que lo garantiza, pero **UDP** no garantiza la transmisión fiable.

_¿Se puede recuperar una información que llega dañada o que simplemente no llega?_ Tanto **TCP** como **UDP** tiene comprobación de errores, cuando se recibe una información dañada o no llega, se retransmite.

_¿Nos garantizan los protocolos de transporte como TCP y UDP la entrega correcta de los datos?_ **TCP** sí, **UDP** no.