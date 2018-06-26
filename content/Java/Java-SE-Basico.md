# Java SE Básico

Java tiene la filosofía: _**Write Once Run Anywhere**_ **WORA**, quiere decir que cualquier código que escribas lo escribirás solo una vez pero lo podras ejecutar siempre que lo necesites.

## 1. Introducción a Java

### ¿Qué es Java?

Java es un lenguaje de programación de alto nivel, esto significa que tiene menos contacto con el hardware.

Tiene como caracteristiacas resaltantes:

+ **Simple**

    + Basado en **C**, la sitaxis es muy parecida a **C** y **C++** (OOP)
  
    + Se hereda de una sola clase
  
    + Clase _String_, que no existe en **C** ni en **C++**
  
    + _Garbage Colector_, se encarga de remover los objetos que no estan en uso para liberarlos de la memoria para hacer mas eficiente el lenguaje
  
+ **Orientado a Objetos**

    + Es un paradigma, tiene su teoria, filosofia. Muy importante aprenderla como tal.
    
    + Java como tal es Lenguaje Oriendato a Objetos.

+ **Distribuido**

    + Diseñado para trabajar con protocolos **TCP/IP**, **HTTP**, **FTP**, etc. Todo lo necesario para trabajar en ambientes de redes.

+ **Multihilo**

    + Tenemos mayor procesamiento en las computadoras o telefonos.
      
      Un Ejemplo, la clase Thread para trabajar con procesos que ocurren al mismo tiempo al paralelo, dos o mas procesos.

+ **Arquitectura Neutral**

    + Corre no solo en un ambiente de trabajo(no solo Windows o Linux)

+ **Portable**

    + Corre en varios sistemas operativos.

+ **Alto desempeño**

    + Es Compilado e Interpretado que lo hace tener un alto desempeño

+ **Seguro**

    + Gracias a la Maquina Virtual (JVM)
    
    + El código no esta expuesto a nadie ya que a la hora de compilar lo convierte a ByteCode(archivo _.class_) y a la hora de correr el programa no lee el codigo fuente.


### El origen de Java

Java nació en 1991 su creador es [James Gosling](https://es.wikipedia.org/wiki/James_Gosling), Java fue adquirido por sus microsystems cuando James Gosling creó el lenguaje.

_¿Porqué se dio la necesidad de crear este lenguaje?_ Por la comunicación entre dispositivos, se requiería que los dispositivos tuvieran un software que podemos controlar, java surgió para satisfacer la necesidad de portabilidad de los dispositivos.

Java es un lenguaje que se originó para ser ampliamente portable.

En el año 2009 Oracle compró a Java, esto hizo que el sistema de certificaciones creciera.

Java SE (es la base de Java).

Java se utiliza muchísimo en el backend de cualquier tipo de aplicación, para esto se usa la versión Enterprise Edition.


## Java en Linux

Para instalar solo se debe ejecutar los siguientes comandos en terminal

```sh

  sudo apt-get update

  sudo add-apt-repository ppa:linuxuprising/java

  sudo apt update

  sudo apt install oracle-java10-installer # version 10

  java -version

  javac -version

```

## 2. Tipos de Datos

En Java existen ocho tipos de datos primitivos que se pueden clasificar en:


+ Números enteros (byte, short, int, long).

+ Números reales (float, double).

+ Carácter (char).

+ Booleano o lógico (boolean).

De todos ellos, salvo del tipo boolean que únicamente puede ser true o false, en la siguiente tabla se muestran sus posibles valores 
mínimo y máximo:

### Lista de tipos de datos primitivos del lenguaje Java


**byte** 8 bits  -128  127

**short** 16 bits -32768  32767

**int** 32 bits -2147483648 2147483647

**long** 64 bits -9223372036854775808  9223372036854775807

**float** 32 bits -3.402823e38  3.402823e38

**double** 64 bits -1.79769313486232e308 1.79769313486232e308

**char** 16 bits ‘\u0000’  ‘\uffff’

_Nota_: un dato de tipo carácter se puede escribir entre comillas simples, por ejemplo ‘a’, o también indicando su valor Unicode, por ejemplo ‘\u0061’.

### Naming en Java

Reglas que Java tiene para la declaración de variables:

+ Java es sensible a mayúsculas y minúsculas.

+ Pueden comenzar con ``_`` o ``$``

+ No pueden comenzar con numeros

+ Las constantes se escriben en Mayúsculas

+ CamelCase -Uper Camel Case para los nombres de las clases y nombres de archivos, es decir que la primera letra que escriba debe ser mayúscula. Lower Camel Case - para nombres de variables, objetos y metodos, quiere decir que la primera letra que escriba debe ser en minúscula.