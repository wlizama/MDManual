# Eloquent ORM
**ORM** según [Wikipedia](https://es.wikipedia.org/wiki/Mapeo_objeto-relacional) es _una técnica de programación para convertir datos entre el sistema de tipos utilizado en un lenguaje de programación orientado a objetos y la utilización de una base de datos relacional como motor de persistencia._

Eloquent es el **ORM** que laravel ofrece.

**Eloquent** proporciona una implementación de ActiveRecord bella y sencilla para trabajar con su base de datos. Cada tabla de base de datos tiene un "Modelo" correspondiente que se utiliza para interactuar con esa tabla. Los modelos le permiten consultar datos en sus tablas, así como insertar nuevos registros en la tabla.

## Definiendo Modelos
Los modelos generalmente viven en el directorio de la aplicación, pero puede colocarlos en cualquier lugar que se puedan cargar automáticamente de acuerdo con su archivo ``composer.json``. Todos los modelos Eloquent amplían la clase ``Illuminate\Database\Eloquent\ Model``.

La forma más sencilla de crear una instancia de modelo es utilizando el comando ``make:model`` de Artisan:

```sh
  php artisan make:model User
```