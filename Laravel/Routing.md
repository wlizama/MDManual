# Routing
Las rutas más básicas de Laravel simplemente aceptan una URI y un _**Clousure**_, proporcionando un método muy simple y expresivo para definir rutas:

```php
  Route::get('hi', function () {
    return 'Hello World';
  });
```

### Los archivos de ruta predeterminados
Todas las rutas de Laravel se definen en los archivos de ruta, que se encuentran en el directorio ``routes``. Estos archivos son cargados automáticamente por el framework. El archivo ``routes/web.php`` define rutas que son para su interfaz web. A estas rutas se les asigna el grupo de middleware ``web``, que proporciona características como estado de sesión y protección CSRF. Las rutas en ``routes/api.php`` son apátridas y se les asigna el grupo de middleware ``api``.

### Métodos de Router disponibles
```php
  Route::get($uri, $callback);
  Route::post($uri, $callback);
  Route::put($uri, $callback);
  Route::patch($uri, $callback);
  Route::delete($uri, $callback);
  Route::options($uri, $callback);
```

A veces puede necesitar registrar una ruta que responda a múltiples verbos HTTP. Puede hacerlo usando el método de ``match``. O bien, puede incluso registrar una ruta que responda a todos los verbos HTTP utilizando cualquier ``any``:

```php
  Route::match(['get', 'post'], '/', function () {
    //
  });

  Route::any('foo', function () {
    //
  });
```

### Redirigir rutas
Si está definiendo una ruta que redirecciona a otro URI, puede usar el método ``Route::redirect``. Este método proporciona un acceso directo conveniente para que no tenga que definir una ruta completa o un controlador para realizar una redirección simple:

```php
  Route::redirect('/here', '/there', 301);
```

### Rutas y Vistas
Si su ruta solo necesita devolver una vista, puede usar el método ``Route::view``. Al igual que el método de redireccionamiento, este método proporciona un acceso directo simple para que no tenga que definir una ruta completa o un controlador. El método de vista acepta un URI como su primer argumento y un nombre de vista como su segundo argumento. Además, puede proporcionar un array para pasar a la vista como un tercer argumento opcional:

```php
  Route::view('/welcome', 'welcome');

  Route::view('/welcome', 'welcome', ['name' => 'Taylor']);
```


### Parámetros de ruta
Por supuesto, a veces necesitará capturar segmentos del URI dentro de su ruta. Por ejemplo, puede que necesite capturar la ID de un usuario de la URL. Puede hacerlo definiendo parámetros de ruta:

```php
  Route::get('user/{id}', function ($id) {
      return 'User '.$id;
  });

```

Puede definir tantos parámetros de ruta como requiera su ruta:

```php
  Route::get('posts/{post}/comments/{comment}', function ($postId, $commentId) {
      //
  });
```

Los parámetros de ruta siempre están encerrados dentro de ``{}`` llaves y deben consistir en caracteres alfabéticos, y no pueden contener un carácter ``-``. En lugar de usar el carácter ``-``, use un guión bajo ``(_)``. Los parámetros de ruta se inyectan en las devoluciones/controladores de ruta en función de su orden; los nombres de los argumentos de devolución de llamada / controlador no importan.

### Parámetros Opcionales
Ocasionalmente, puede que necesite especificar un parámetro de ruta, pero haga que la presencia de ese parámetro de ruta sea opcional. Puede hacerlo colocando un ``?`` después del nombre del parámetro. Asegúrese de dar a la variable correspondiente de la ruta un valor predeterminado:

```php
  Route::get('user/{name?}', function ($name = null) {
      return $name;
  });

  Route::get('user/{name?}', function ($name = 'John') {
      return $name;
  });
```

### Restricciones de expresiones regulares
Puede restringir el formato de los parámetros de ruta utilizando el método ``where`` en una instancia de ruta. El método ``where`` acepta el nombre del parámetro y una expresión regular que define cómo se debe restringir el parámetro:

```php
  Route::get('user/{name}', function ($name) {
      //
  })->where('name', '[A-Za-z]+');

  Route::get('user/{id}', function ($id) {
      //
  })->where('id', '[0-9]+');

  Route::get('user/{id}/{name}', function ($id, $name) {
      //
  })->where(['id' => '[0-9]+', 'name' => '[a-z]+']);
```