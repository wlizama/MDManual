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