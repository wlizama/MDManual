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

