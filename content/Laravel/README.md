# Laravel

**Laravel** es un framework de código abierto para PHP. Su filosofía es desarrollar código PHP de forma elegante y simple, evitando el "código espagueti". 

## Requerimientos básicos de Laravel.
* PHP >= 7.0.0
* OpenSSL PHP Extension
* PDO PHP Extension
* Mbstring PHP Extension
* Tokenizer PHP Extension
* XML PHP Extension

En sistemas Linux y Mac, esto se podrá hacer a través del administrador de paquetes, así como instalamos el lenguaje. 

```sh
    $ sudo apt-get install php7.1-openssl
```

## Instalar composer
**Composer** es una herramienta para administrar dependencias de código PHP. 

#### Instalacion Global
Para descargar la versión más reciente de Composer y convertirla en un comando del sistema:

```sh
    $ curl -sS https://getcomposer.org/installer | php
    $ sudo mv composer.phar /usr/local/bin/composer
```

## Instalar Laravel Installer
Laravel provee un ejecutable para comenzar nuevos proyectos. Este ejecutable se instala como una dependencia global de composer y nos permitirá crear proyectos Laravel de una forma rápida.

```sh
    $ composer global require "laravel/installer"
```

Después de esto agregar el directorio de ejecutables instalados globalmente por composer a tu variable de entorno PATH.

```sh
    vim /home/[nombre_usuario]/.bashrc 
```

Agregar al final del archivo:

```sh
    export PATH=$PATH:$HOME/.config/composer/vendor/bin
```

Para usar el instalador de laravel, navegamos a la carpeta donde queremos tener nuestro código fuente y ejecutamos:

```sh
    laravel new mi-proyecto
```

El instalador creará una nueva carpeta llamada _“mi-proyecto”_ y descargará todo el código necesario para un proyecto Laravel.

Si tiene PHP instalado localmente y desea utilizar el servidor de desarrollo incorporado de PHP para servir su aplicación, puede usar el comando ``serve`` Artisan. Este comando iniciará un servidor de desarrollo en ``http://localhost:8000``

```sh
    php artisan serve
```

---

## Enlaces de interés

+ [Documentación oficial de Laravel](https://laravel.com/docs/5.6)
