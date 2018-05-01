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

## Import

_CSS_ tiene una opción de importación que le permite dividir su CSS en partes más pequeñas y más fáciles de mantener. El único inconveniente es que cada vez que utiliza @import en CSS crea otra solicitud HTTP. Sass se basa en el @import CSS actual, pero en lugar de requerir una solicitud HTTP, Sass tomará el archivo que desea importar y lo combinará con el archivo que está importando para que pueda servir un único archivo CSS en la web. navegador.

Suponiendo que tenemos un archivo ``_button.scss`` y lo queremos importar a ``main.scss``

```scss
  //_button.scss

  button{
    color : #CCC;
    border-radius : 2px
  }
```


```scss
  //main.scss

  $color : red !default;
  $color2 : yellow !default;
  $color3 : green !default;

  .div{
    background-color : $color;
    color : $color2
  }

  @import "_button";
```

**Output .css**

```css
  .div {
    background-color: red;
    color: yellow;
  }

  button {
    color: #CCC;
    border-radius: 2px;
  }

```