# Sass

Según su página web oficial [https://sass-lang.com/](https://sass-lang.com/)

>Sass es el lenguaje de extensión CSS de grado profesional más maduro, estable y poderoso del mundo.

## Variables

Se puede almacenar valores como colores, fonts stack o cualquier valor de CSS que crea que desea reutilizar. Sass usa el símbolo $ para hacer que algo sea una variable. Aquí hay un ejemplo:

**.Scss**

```scss
  $font-stack:    Helvetica, sans-serif;
  $primary-color: #333;

  body {
    font: 100% $font-stack;
    color: $primary-color;
  }
```

**Output .css**

```css
  body {
    font: 100% Helvetica, sans-serif;
    color: #333;
  }
```