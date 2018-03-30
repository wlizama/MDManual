# Django

Es un Framework Python y según su página [https://www.djangoproject.com/](https://www.djangoproject.com/):

>_Django es un framework web Python de alto nivel que fomenta un desarrollo rápido y un diseño limpio y pragmático. Desarrollado por desarrolladores experimentados, se encarga de gran parte de las complicaciones del desarrollo web, por lo que puede concentrarse en escribir su aplicación sin necesidad de reinventar la rueda. Es gratis y de código abierto._

### Ridiculosamente rápido

Django fue diseñado para ayudar a los desarrolladores a llevar las aplicaciones desde el concepto hasta su finalización lo más rápido posible.

### Tranquilo y seguro

Django toma en serio la seguridad y ayuda a los desarrolladores a evitar muchos errores comunes de seguridad.

### Extremadamente escalable

Algunos de los sitios más concurridos de la Web aprovechan la capacidad de Django para escalar rápida y flexiblemente.


## Configuración del proyecto - settings

**Database**: Aquí van nuestras base de datos. Podemos tener una o varias configuradas.

**Installed Apps**: Aplicaciones instaladas por defecto tiene varias ya instaladas(sesiones, mensajes, archivos estáticos). Django va a reconocer lo que esta ahí como parte de nuestro proyecto.

**Allowed host**: Este setting necesita estar activo si el modo debug esta desactivado. Básicamente nos protege en contra de un ataque y colocamos los host de nuestro de proyecto en producción.

**Middleware**: Cuales están activos, cada Middleware representa una lógica, unos hooks, que podemos implementar en nuestro proyecto.

**Debug**: Si esta activo este modo, nos dará mas información sobre nuestros errores. Como los patrones de urls, se puede ver mas fácil como corregirlos.

## Function Based View

Las vistas basadas en funciones nos permiten procesar las solicitudes del usuario a través de funciones.

**Function Based-Views**: Vistas basadas en funciones, recibe un request, se procesa y se responde con un HttpResponse

**Request**: Contiene toda la información de todo nuestro request, por ejemplo si hay parametro GET dentro del request vienen esos parametros.

**HttpResponse**: Con este podemos retornar los valores dentro del request.

Siempre es buena practica que tengan la carpeta templates en cada app que tenga la aplicación. Así como también un archivo urls.py en ellas, para tener el código más pequeño y modular.

## Class based-views

Es una clase en vez de una función que hereda de clase que se llama view. Implementa al menos un método dispatch o **GET** o **POST**.

**Dispatch**: Ejecuta ambos métodos GET y POST o puede ser que solamente tengamos uno de ellos.

**Ventajas sobre las vistas basadas en funciones**: Podemos tener herencia, implementar mixing, podemos tener comportamiento por defecto.

**CreateView**: Se genera con un formulario y se crea un nuevo modelo.

**UpdateView**: Ya trae una instancia de un modelo y simplemente lo actualiza.

**ListView**: Hace un listado de los objetos de un modelo

**DeleteView**: Borra un objeto de un modelo.

## Uso de templates o plantillas

Los Templates son la parte de la vista si hacemos relación con el modelo **MVC**.

En nuestro proyecto de Django debemos crear una nueva carpeta llamada templates dentro de cada aplicación, y luego en la carpeta templates debemos crear una nueva carpeta con el nombre de la aplicación para que este sea el namespace.

Los Templates son plantillas que reciben datos y generan código HTML. Para los Templates debemos manejar una sintaxis un poco diferente.

```
{{ variable }}

{% cycle 'odd' 'even' %}

{% if conditiion %} print_something() {% endif %}

{{ my_date|date:“Y-m-d” }}

```

## Context Processor

Podemos compartir variables en múltiples templates. Definimos un diccionario y esos valores se van a agregar a todos nuestros templates.

_Cuando usarlos_: Si se usan muchas vistas o en todas las vistas, si es algo muy global lo mejor es que uses _Context Processors_.

## Herencia e Inclusión / extend e include

En los Templates tenemos dos opciones que podemos usar y que nos permiten reducir la cantidad de código que debemos escribir.

**Inclusión: {% include %}** Es similar tenemos un código que se repite en muchos sitios y lo incluimos.

**Herencia: {% extends % }** Significa que tenemos un template base y en base a ese podemos heredar y ocupar el código de un template especifico.