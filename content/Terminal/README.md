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


## Monitoreo de procesos

+ **``echo``** Imprime una cadena, _Ejm_: **``echo $PATH``**

+ **``which``** Muestra la ruta del programa que se esta ejecutando, _Ejm_: **``which bc``**

+ **``top``** Muestra un estatus del sistema (en tiempo real), se puede ordenar según CPU, MEM, etc.

>_**Nota:** Cada proceso tiene su propio PID (Identificación de Proceso)_

Para saber el Output del proceso ejecutado anteriormente ejecuta **``echo $?``**, si el estatus es diferente a 0 (cero) es porque el proceso no finalizó de forma correcta.


## Standard Input, Output
+ **Mayor que ``>``:** Manda todas las salidas output a un archivo, sí el archivo no existe lo crea, sí existe lo reescribe añadiéndole líneas nuevas (con la información de la operación realizada).

+ **Menor que ``<``:** Lee un archivo y manda el output a un programa que lo leerá ese resultado como input.

+ **Mayor, mayor que ``>>``:** Tiene la misma función que > con la diferencia que este suma, concatena los resultados en un archivo.

+ **Para concatenar Outputs ``|``**: Se usa ``|``, _Ejm_: **``cat file.txt | bc -q``** (esto leerá el archivo "file.txt" y luego lo ejecutará con el programa bc sin mostrar "el mensaje de bienvenida" ya que la bandera -q omite eso).


## Búsqueda de contenido en archivos, carpetas, y uso de Grep

+ **``grep "[texto]" [archivo o directorio]``** Busca dentro de un archivo una cadena de texto ("string"), _Ejm_: **``grep "joaqnjs" archivo.csv``**.

    + **``-r``** Esta bandera sirve para buscar recursivamente.

    + **``-e``** Esta bandera determina la expresión a buscar.

    + **``-n``** Esta bandera nos muestra el nombre del archivo y la línea.

    + **``-v``** Esta bandera busca una cadena de string y si la encuentra no la imprime, es decir, imprime las no coincidencias.

    + **``^``** Indica el inicio (o desde el inicio) de línea.

    + **``$``** Indica el fin (o hasta el fin) de línea.

+ **``find [directorio] -name "[texto]"``** Busca por nombre de archivos.

    + **``-type f``** Especifica que es un archivo.

    + **``-exec [comando]``** Al finalizar la busqueda ejecuta un comando. Un comando para renombrar todos los archivos que coincidan es: mv {} {}.txt \: Las llaves hacen referencia al archivo que se encontró {}.

+ **``split -l [cantidad de líneas] [archivo] [destino]``** Rompe un archivo en la cantidad de líneas que se determine y los resultados lo guarda en un destino.


## Peticiones HTTP desde la terminal con CURL

**``curl https://www.google.co.ve``** Trae todo el código html y lo muestra en la terminal.

+ **``-o``** Esta bandera guarda en un archivo (que si no existe lo crea) el output de la operación con **``curl``**, _Ejm_: **``curl -o google.html https://www.google.co.ve``**

+ **``-O``** Trae un archivo y lo descarga desde la web.

_Método get: **curl http://httpbin.org/get?variable=1**_

_Método get "con más de 1 variable": **curl "http://httpbin.org/get?variable=1&constante=10"**_

_Método post: **curl --data "numOne=1&numTwo=2" http://httpbin.org/post**_

>**Nota:** Para cambiar el _User-Agent_ se hace con la bandera **``-A``** seguido del "nombre del agente", por ejemplo: **``curl -A "Agente_JoAQNjs"``**


## Crontab

Con **``crontab -e``** se programan tareas que se ejecuta según sea especificado mientras la computadora esta encendida, mientras el sistema este operando.

+ **``-l``** Imprime los crontabs existente, instalados en un usuario. Cada usuario del sistema tiene un crontab diferente.


**Crontab** esta compuesto por 5 valores importantes:

![image](https://raw.githubusercontent.com/wlizama/MDManual/master/assets/images/linux-crontab.png "Crontab Linux")

Un Script de ejemplo sería el de guardar la fecha cada minuto, todos los dias a las 12 horas (formato 24h).

```sh
    * 12 * * * date >> /tmp/date
```

En el directorio **``/etc/cron.[frecuencia]``** existen una serie de archivos, en ellos se puede configurar algún script (o comando) que necesitemos ejecutar con "equis" frecuencia, de esta forma el Crontab queda guardado de forma permanente.