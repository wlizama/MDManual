# Introducción a la Terminal

Comandos básicos para terminales UNIX.

## Navegación entre directorios y listado de archivos

+ **``pwd``** Muestra la ubicación, la ruta del directorio donde se encuentra posicionado.

+ **``~``** Es la "Home" del usuario. _Ejm_: /home/wilder

+ **``/``** Es la "Raiz" del Sistema Operativo

+ **``ls``** Lista los archivos o carpetas (del directorio donde se encuentra al momento de ejecutar el comando)
    
    + **``-l``** Esta bandera lista los archivos de un directorio como una lista y muestra algunos detalles importantes, como por ejemplo: Tipo de archivo (d, -, l), permisos, propietario, tamaño, fechas de creación, etc.

    + **``-t``** Esta nos ordena los archivos desde los más recientes hasta los más viejos (según su fecha de creación).

    + **``-r``** Esta bandera revierte las funciones de las banderas anteriores, por ejemplo: -ltr listaría los archivos y directorios desde el más antiguo al más reciente.

    + **``-h``** Esta bandera ("legible humanamente") nos muestra el tamaño de los archivos en Bites, Kilobytes, Megabytes, etc.


    + **``-S``** Esta bandera ordena los archivos y/o directorios desde el más pesado al menos pesado, un buen uso sería: **``-lhS``** de esta forma estarías listando, mostrando el tamaño de una forma legible (para un humano) y ordenandolos.


+ **``cd``** Nos ayuda a movernos entre directorios, con ``TAB`` podemos ver los archivos o directorios existentes (en la ubicación).

+ **``du -h``** Muestra el peso total de los directorios.

>_**Nota:** Las banderas se pueden concatenar (no en todos los comandos funcionan) escribiendo despúes del guión (-) las banderas, por ejemplo: **``-lt``**_


## Creación de directorios, mover, copiar, y renombrar archivos

+ **``mkdir``** Crea un nuevo directorio.

+ **``touch``** Abre el archivo y lo cierra, también con este comando se puede crear un archivo (incluso hasta se le puede añadir la extensión), por ejemplo: touch index.html

+ **``mv``** Mueve un archivo o un directorio. _Ejm_: **``mv ../photo.jpg /.``**

+ **``cp``** Copia un archivo o un directorio. _Ejm_: **``cp ./photo.jpg ../``**

>_**Nota:** Colocar un * (asterisco) seguido de una extensión nos ayuda a ejecutar un comando a todos los archivos con esa extensión, puede ser, moverlos, copiarlos, borrarlos, etc._


## Programas desde la terminal

+ **``bc``** Es una calculadora básica. Para salir escribir **``quit``**.

>_**Nota:** Una bandera muy práctica de **``bc``** es **``-q``**, esta nos ayuda a "omitir el mensaje de bienvenida de dicha calculadora" y nos manda directamente a ejecutar operaciones._

+ **``open``** Abre un archivo con el programa que el sistema crea más conveniente.

>_**Nota:** A el comando **``open``** se le puede agregar una bandera para especificar el programa que deseas para abrir el archivo, esa bandera es: **``-a``** seguido del programa, Ejm: **open -a subl file.txt**_

+ **``mb5``** Muestra la huella digital de un archivo.

+ **``more``** Imprime una parte de un archivo (para leerlo desde la terminal). Para salir se presiona la letra **``q``**.

+ **``tail``** Imprime las últimas 10 líneas del archivo.

    + **``-20``** Esta bandera muestra las últimas 20 líneas (se puede imprimir el número deseado).
    
    + **``-f``** Esta bandera mantiene activamente en modo "de escuchar" un archivo, esto sirve para desarrollar, muestra logs, etc.

+ **``cat``** Concatenación. Imprime todo el archivo, la diferencia con **``more``** es que no lo página.

+ **``wc``** Cuenta el número de líneas, palabras y caracteres.

    + **``-l``** Esta bandera muestra todas las líneas que tiene.
    
    + **``-w``** Esta bandera muestra todas las palabras que tiene.
    
    + **``-c``** Esta bandera muestra todos los caracteres que tiene.

## Documentación disponible desde la terminal

+ **``man``** Manual. Este comando seguido de otro nos explica para que funciona un comando y nos dice las banderas que tiene.