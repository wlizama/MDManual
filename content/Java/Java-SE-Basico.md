# Java SE Básico

Java tiene la filosofía: _**Write Once Run Anywhere**_ **WORA**, quiere decir que cualquier código que escribas lo escribirás solo una vez pero lo podras ejecutar siempre que lo necesites.

## 1. Introducción a Java

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