# Controllers
Los controladores pueden agrupar la lógica de manejo de peticiones en una sola clase. Los controladores se almacenan en el directorio ``app/Http/Controllers.``

### Definiendo Controladores
El controlador extiende de la clase de ``Controller`` incluida con Laravel. La clase ``Controller`` proporciona algunos métodos de conveniencia, como el método de middleware, que se puede usar para adjuntar middleware a las acciones del controlador:

```php
    namespace App\Http\Controllers;

    use App\User;
    use App\Http\Controllers\Controller;

    class UserController extends Controller
    {
        /**
         * Show the profile for the given user.
         *
         * @param  int  $id
         * @return Response
         */
        public function show($id)
        {
            return view('user.profile', ['user' => User::findOrFail($id)]);
        }
    }
```

Puede definir una ruta a esta acción de la siguiente manera:

```php
    Route::get('user/{id}', 'UserController@show'); //nameController@method
```

