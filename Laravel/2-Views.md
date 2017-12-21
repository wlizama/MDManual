# Views
Las vistas contienen el HTML de su aplicación y separa la lógica de su controlador. Las vistas se almacenan en el directorio ``resources/views``. Una vista simple podría verse más o menos así:

```php
  <html>
      <body>
          <h1>Hello, {{ $name }}</h1>
      </body>
  </html>
```
