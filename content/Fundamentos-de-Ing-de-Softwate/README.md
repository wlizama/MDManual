# Fundamentos de Ingeniería de Softwate

En este curso se conoceran los conceptos que dan vida a internet, computación, sistemas operativos, etc...

## 1. Computación, procesadores y memoria

### Qué es un system on a chip

Es todo el sistema de funcionamiento de un CPU normal de computadora, integrado en un Chip.

La arquitectura rápida y compleja en un sistema tradicional podemos hoy tenerlo en un disposivo pequeño gracias a un system on a chip.

Un **System on a Chip** es una CPU que también tiene una memoria RAM y un disco duro en un chip.

También incluye chips especializados que permiten realizar algunos procesos necesarios por un dispositivo móvil.

### Qué son Bits y Bytes

**Bit**

Su nombre es el acrónimo de _Binary Digit_ y es la unidad más pequeña de almacenaje que puede tomar un ordenador. Sus opciones se reducen a dos, tomando el valor de 0 o de 1. Por lo tanto, es un tipo de dato binario, ya que de esta manera, es mucho más sencillo de interpretar por los dispositivos electrónicos.

**Byte**

Es la unidad de capacidad de almacenamiento estándar. Con esta unidad de medida se mide desde el almacenamiento de datos hasta la capacidad de memoria de un ordenador.

Representa un carácter (un número, una letra, un espacio, o cualquier otro signo) y está constituido por 8 bits consecutivos, de modo tal que un byte equivaldría a 8 bits.

Hay 256 combinaciones de 8 bits posibles, por lo que hay 256 caracteres.

![image](https://raw.githubusercontent.com/wlizama/MDManual/master/assets/images/Bit-byte.jpg "Qué son Bits y Bytes")

### Procesadores y arquitecturas de CPU

Existe una arquitectura para computadores de escritorio y laptops, estos internamente tienen:

**CPU - Central Processing Unit:** Procesador central (con marcas como Intel, AMD). Para conocer la capacidad de tu CPU te guías por los GHz (velocidad a la que procesan una instrucción) y Cores (# de CPU’s en un mismo chip, cuantas instrucciones pueden hacer al mismo tiempo).

**BIOS:** Chip especial que está instalado en la tarjeta madre, es un sistema operativo de arranque. Cuando arranca intenta detectar todas las cosas que están conectadas a un computador (perifericos como : pantalla, teclado, mouse, puertos, etc...).

**Disco Duro:** Es dónde se guarda toda la información, aqui está el sistema operativo.

**RAM - Random Access Memory:** Es un tipo de intermediario entre el Sistema Operativo que está en el disco duro y el CPU. Es una memora de alta velocidad (memoria volátil), sólo funciona cuando hay electricidad.

**Memristor:** Pieza electrónica que logra guardar la onda eléctrica que pasa por ella incluso cuando se desconecta. Es posible que sea el reemplazo del disco duro y la memoria RAM en el futuro.

**Periféricos:** Pantalla, teclado, mouse, puertos, etc.

**Drivers:** Convierte la interacción de los accesorios periféricos en Bits y Bytes para que el computador pueda entender las instrucciones que les damos a través de ellos.

**GPU:** Canal de comunicación entre la pantalla y el CPU. Es quién se encarga de mostrar todo en la pantalla, desde que arranca hasta reproducir videos y videojuegos.

### Qué es la memoria RAM y cómo funcionan los discos duros

Discos duros:

+ Forma en que organizan datos:

  + Persistente

  + Secuencial

  + Estructurada (Depende del sistema de archivos, que a su vez depende del S.O. que esté en el disco duro):

    + Windows: FAT16 - FAT32, NTFS

    + Linux: Ext3 - Ext4

    + Mac OS: HFS, APFS

+ Forma de localizar y leer archivos:

  En la parte superior de los Discos Duros existe una cabecera, la cual guarda el indice de todos los archivos, esto permite que en el momento de lectura desde la cabecera, se conozca en dónde está ubicado el archivo en cuestión.

+ Borrado de archivos:

  Por tal motivo, cuando se “borra” un archivo, lo que realmente se esta haciendo es eliminando el indice en la cabecera que está relacionado con el archivo. Determinados tipos de software permiten la recuperación de estos archivos, leyendo detalladamente toodo el disco duro. Sin embargo algunas practicas de borrado (Sheredder) permiten borrar el archivo por completo, incluso ejecutando el borrado determinado número de repeticiones, lo que imposibilita el trabajo de forenses para la recuperación de datos o archivos.

**Memoria RAM (Random access memory)**

+ Procesos:

  La memoria RAM, siendo tan rápida, tiene la capacidad de ejecutar varios procesos paralelamente. El SO es uno de esos procesos ejecutados por la RAM. Sin embargo la opciones que nos ofrece el SO son muchas y no siempre se utilizan todas, por lo tanto la RAM solo carga aquellas tareas que realmente necesitamos y estamos usando frecuentemente.

+ Localización de procesos:

  A diferencia de los discos duros, la memoria RAM hace uso de un indice compartido con la CPU que es ultra veloz. Esto facilita y permite una localización de los procesos por parte de la CPU de una manera increíblemente rápida.

**CPU (Central process unit):**

+ Dentro de este asombroso chip, no encontramos con un espacio que recibe por nombre Memoria Caché. En ella se guardan y almacenan cierto tipo de datos de uso frecuente, para que sea más fácil y rápido el acceso a ellos. Por ejemplo una parte del SO siempre estará almacenada en la Memoria Caché para que sea rápido acceder a él.

+ Comunicación:

  + Ram:
    
    Para lograr la efectiva comunicación entre la CPU y la RAM existe lo que se conoce como un bus de datos o bridge (puente). Un bus de datos en algunas ocaciones es un cable delgado y ancho. En otros casos esta conexión está establecida como circuito en la placa madre (mother board).

  + Disco Duro:
    
    Para la conexión entre en disco duro y la CPU, el bus de datos recibió inicialmente el nombre ATA, que en una versión posterior se llamó SATA. Hay otro tipo de bus de datos para el disco duro mejor que SATA, que se llamó IDG.

### GPUs, tarjetas de video y sonido

¿Cómo veo en pantalla que el archivo se ha abierto?

Esto se logra gracias a la **Graphic Processing Unit o GPU**.

La CPU puede ejecutar cualquier proceso, incluido el dibujado en pantalla de ciertos datos. Pero no es ella quien se encarga, sino la GPU: tarjetas especialmente fabricadas para realizar estas tareas.

La comunicación entre la CPU y la GPU se realiza actualmente a través de un socket llamado PCI-Express.

Estas placas de vídeo tienen sus propias unidades o núcleos de procesamiento y su propia memoria RAM.

Lo que sucede es que la GPU divide la pantalla en una matriz y cada núcleo se encarga de dibujar una parte de esa matriz, para lograr una mejor performance.

Esto es mucho más rápido de lo que podría lograr la CPU sola ya que debería dibujar pixel por pixel ella sola.

**Entonces haciendo una analogía**

_El GPU es como el **Front-End** del software, se encarga de que todos los gráficos de la computadora se vean y funcionen perfectamente bien._

_Haciendo que el CPU deje de preocuparse por eso y se enfoque en otros tipos de procesamiento._

### Periféricos y sistemas de entrada de información

Los sistemas operativos normalmente tienen un núcleo llamado kernel, que es el principal elemento que los representa y es la primera parte del sistema operativo que se carga en la memoria RAM. El kernel del sistema operativo tiene acceso a todo en nuestra computadora: nuestros archivos, a nuestros periféricos, a los datos de las aplicaciones.

El kernel, inmediatamente después de ser cargado en RAM, se encarga de cargar los drivers: pequeñas piezas de software que permiten interpretar las señales eléctricas del hardware, para que el sistema operativo pueda comunicarse con ellos.

Luego tenemos otro set de drivers que pueden ser los controladores de arranque llamados drivers de aplicación. Cuanto más nos alejamos del kernel, menos privilegios tenemos. Los drivers de aplicación deben pedirle permisos a los drivers anteriores para poder acceder al hardware.

La última capa la representan las aplicaciones. Esta es la capa que menos permisos tiene, ya que las aplicaciones no deberían poder acceder al hardware directamente.

### Arquitectura de la computación

En el inicio de la computación no existía un procesador y una memoria aparte. Las computadoras estaban más cerca de ser una máquina de escribir que una de las computadoras que conocemos ahora. Eran máquinas grandes y pesadas, que requerían ser trasladadas en aviones o camiones. El código binario se escribía en tarjetas perforadas: cuyas perforaciones (o falta de ellas) representaban los 1 y 0.

Hoy en día tenemos computadoras en nuestros propios bolsillos y las cargamos a todos lados, tenemos laptops cuyos monitores se pueden desacoplar y funcionan como tablets, tenemos microchips que sirven como una computadora común y corriente.

Ese salto evolutivo en la computación ocurre gracias a la estandarización de la arquitectura de las computadoras: decidimos que un Byte son 8 bits, que la CPU es la encargada de procesar, que la GPU representa datos visualmente, que 1024 Bytes son un KiloByte, y que 1024 KB son 1 MB, que exista un puerto común como el USB que nos permite conectar otros dispositivos externos.

Estandarizamos la transferencia de datos y los protocolos de comunicación. Hay un formato definido para cada tipo de imágenes, hay una forma de escribir HTML para que el navegador lo interprete y pueda mostrarnos elementos visuales en la pantalla. Definimos una forma para comprimir un archivo.

## Cómo funciona internet

### Puertos y protocolos de red

Como funcionan y cuales son las direcciones IP, quien las asigna a nivel publico y como los router a través de DHCP asignan las privadas.

Cuantos rangos de ip tenemos disponibles y mencionan algunos puertos y para que se usan.

+ IP’s que dirigen a nuestro pc:
  
  + 127.0.0.1
  
  + 192.168.0.1 (Ip de LAN )
  
  + localhost (host)

+ Puertos: Redes virtual dentro del SO

  Se puede hacer una analogía con los cables y pines, por lo que enviamos información en un circuito. En un SO funcionan los puertos

  + Del 1 al 1024 (llamados bien conocidos) están reservados para ser ejecutados por el SO a través del admin.

    **Ejemplos:**
    
    + 1 - Protocolo HTTP => Puerto 80
    
    + 2 - Protocolo HTTPS => Puerto 443
  
  + Del 1024 al 49151 son los puertos registrados, los cuales puede usar cualquier aplicación

    **Ejemplo:**

    + 1 - Bittorrent => Puertos del 6881 al 6889

  + Los puertos del 49151 al 65535 son llamados dinámicos o privados y son aquellos que se asignan dinámicamente a alguna aplicación del cliente, cuando inicia una conexión.

    Ejemplos: Son usados por los servicios P2P (peer to peer)

### Qué es una dirección IP y el protocolo de Internet

**IP**: es la sigla de Internet Protocol y una dirección IP es un número único con el cual una computadora o un dispositivo se identifica cuando está conectada a una red con el protocolo IP.

Cada dirección IP está compuesta por 4 números separados por puntos y son una forma de comprender números más grandes y complejos. Las direcciones IP tienen una estructura que las convierten en privadas o públicas y que además hacen parte de la máscara de red y el getaway.

Las direcciones IP permiten que cada computador o dispositivo pueda conectarse al exterior, es decir a Internet, esto a través de tecnologías como **NAT** o _Network Address Translation_.

**Mascara de red**: La máscara de red o redes es una combinación de bits que sirve para delimitar el ámbito de una red de ordenadores. Su función es indicar a los dispositivos qué parte de la dirección IP es el número de la red, incluyendo la subred, y qué parte es la correspondiente al host. Mediante la máscara de red, un sistema (ordenador, puerta de enlace, router, etc...) podrá saber si debe enviar un paquete dentro o fuera de la subred en la que está conectado. Por ejemplo, si el router tiene la dirección IP ``192.168.1.1`` y máscara de red ``255.255.255.0``, entiende que todo lo que se envía a una dirección IP con formato ``192.168.1.X``, se envía hacia la red local, mientras que direcciones con distinto formato de direcciones IP serán buscadas hacia afuera (internet, otra red local mayor, etc…).

**Gateway**: La pasarela (en inglés _gateway_ ) o puerta de enlace es el dispositivo que actúa de interfaz de conexión entre aparatos o dispositivos, y también posibilita compartir recursos entre dos o más computadoras.

Su propósito es traducir la información del protocolo utilizado en una red inicial, al protocolo usado en la red de destino.

La pasarela es normalmente un equipo informático configurado para dotar a las máquinas de una red de área local (Local Area Network, LAN) conectadas a él de un acceso hacia una red exterior, generalmente realizando para ello operaciones de traducción de direcciones de red(Network Address Translation, NAT). Esta capacidad de traducción de direcciones permite aplicar una técnica llamada "enmascaramiento de IP" (IP Masquerading), usada muy a menudo para dar acceso a Internet a los equipos de una LAN compartiendo una única conexión a Internet, y por tanto, una única dirección IPexterna.

**NAT**: La traducción de direcciones de red o **NAT** (del inglés _Network Address Translation_) es un mecanismo utilizado por routers IP para intercambiar paquetes entre dos redes que asignan mutuamente direcciones incompatibles. Consiste en convertir, en tiempo real, las direcciones utilizadas en los paquetes transportados. También es necesario editar los paquetes para permitir la operación de protocolos que incluyen información de direcciones dentro de la conversación del protocolo.

**_Nota_**

La manera mas facil de ver si una IP es clase A, B o C es utilizando la mascara de red estandar y estas son:

255.0.0.0 - **CLASE A**

255.255.0.0 - **CLASE B**

255.255.255.0 - **CLASE C**

Pero, tambien existe el metodo de máscara de subred variable, la cual es muy util para segmentar una red ip con mascara de red estandar.

Toda seccion representada por un 0 en la mascara de red va a ser destinada a host o clientes y las que estan representadas por 255 son la destinada a la red.

### Cables submarinos, antenas y satelites en Internet

La mayoría de personas imaginan que el acceso a Internet consiste en conexiones satelitales, lo cual es un error, pues los satélites están destinados sólo para áreas remotas. Internet funciona a partir de cables que atraviesan diferentes lugares del mundo.

Cuando usas tu computadora o dispositivo, este se conecta a un ISP o un prestador de servicios de Internet (ese a quién le pagas tu factura). De ahí, la conexión con diferentes puntos en el mundo a través de cables submarinos, que pueden ser de fibra óptica o cobre.

Estos cables pueden comenzar en una ciudad como Nueva York y terminar en Japón y aunque no parezca, la red de Internet un poco frágil pues los cables pueden romperse por diferentes causas, como las anclas de los barcos.


**IXP**

Un punto neutro o punto de intercambio de Internet (_en inglés IXP, Internet Exchange Point_) es una infraestructura física a través de la cual los Proveedores de Servicios de Internet (PSI o ISP, por sus siglas en inglés) intercambian el tráfico de Internet entre sus redes. 

El propósito principal de un punto neutro es permitir que las redes se interconecten directamente, a través de la infraestructura, en lugar de hacerlo a través de una o más redes de terceros. Las ventajas de la interconexión directa son numerosas, pero las razones principales son el costo, la latencia y el ancho de banda.

(Mapa IXPs)[https://www.internetexchangemap.com/]

### Cómo funciona la velocidad en internet

La mayoría de los **ISPs** (_Internet Service Providers_) nos venden ancho de banda en Mb y debemos tener claro qué significa, ya que existe una importante diferencia entre Megabits y MegaBytes.

Otro aspecto importante en el funcionamiento del internet es la velocidad. A menudo confundimos la velocidad con el ancho de banda por eso debemos tener en claro que la velocidad del internet se mide obteniendo el tiempo que le toma a la información viajar a través de un punto a otro en milisegundos, a esto se le conoce como ping o latencia.

La velocidad de nuestro internet se mide en la cantidad de bits no bytes que transmite por segundo

La forma de medir la velocidad de un ping es divididiendo la distancia entre un punto de conexión y otro entre la velocidad de la luz ``300 km/ms``

Distancia entre Mountain View y Madrid 9344 km

``(9344 km)/(300 km/ms) = 31.14 ms``