# Django

Es un Framework Python y segun su página [https://www.djangoproject.com/](https://www.djangoproject.com/):

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
