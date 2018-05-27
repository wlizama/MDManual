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