# Migrations

Las migraciones son como el control de versiones para su base de datos, lo que le permite a su equipo modificar y compartir fácilmente el esquema de la base de datos de la aplicación. Las migraciones suelen combinarse con el generador de esquemas de Laravel para crear fácilmente el esquema de la base de datos de su aplicación.


## Generando Migraciones
Para crear una migración, use el comando ``make:migration`` :

```sh
  php artisan make:migration create_users_table
```

La nueva migración se colocará en el direccorio ``database/migrations``. Cada nombre de archivo de migración contiene una marca de tiempo que le permite a Laravel determinar el orden de las migraciones.

Las opciones ``--table`` y ``--create`` también pueden usarse para indicar el nombre de la tabla y si la migración creará una nueva tabla. Estas opciones simplemente completan previamente el archivo de transición generado con la tabla especificada:

```sh
  php artisan make:migration create_users_table --create=users

  php artisan make:migration add_votes_to_users_table --table=users
```

## Migratios structure

Una clase _Migration_ contiene dos métodos: ``up`` y ``down``. El método ``up`` se usa para agregar nuevas tablas, columnas o índices a su base de datos, mientras que el método ``down`` simplemente debe invertir las operaciones realizadas por el método ``up``. Dentro de estos dos métodos, puede usar el generador de esquemas de Laravel para crear y modificar tablas expresivamente.

**Ejm.**

```php

  <?php

  use Illuminate\Support\Facades\Schema;
  use Illuminate\Database\Schema\Blueprint;
  use Illuminate\Database\Migrations\Migration;

  class CreateFlightsTable extends Migration
  {
      /**
       * Run the migrations.
       *
       * @return void
       */
      public function up()
      {
          Schema::create('flights', function (Blueprint $table) {
              $table->increments('id');
              $table->string('name');
              $table->string('airline');
              $table->timestamps();
          });
      }

      /**
       * Reverse the migrations.
       *
       * @return void
       */
      public function down()
      {
          Schema::drop('flights');
      }
  }
```