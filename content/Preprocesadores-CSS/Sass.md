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

## Anidaciones

Sass te permitirá anidar tus selectores CSS de una manera que siga la misma jerarquía visual de tu HTML. Tenga en cuenta que las reglas excesivamente anidadas resultarán en CSS sobrecargado que podría ser difícil de mantener y generalmente se considera una mala práctica.

**.Scss**

```scss
  nav {
    ul {
      margin: 0;
      padding: 0;
      list-style: none;
    }

    li { display: inline-block; }

    a {
      display: block;
      padding: 6px 12px;
      text-decoration: none;
    }
  }

```

**Output .css**

```css
  nav ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  nav li {
    display: inline-block;
  }

  nav a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
```

## Mixins

Algunas cosas en CSS son un poco tediosas de escribir, especialmente con CSS3 y los muchos prefijos de proveedor que existen. Un mixin le permite crear grupos de declaraciones CSS que desea reutilizar en su sitio. Incluso puede pasar valores para hacer su mixin más flexible.

**.Scss**

```scss

  @mixin border-radius($radius) {
    -webkit-border-radius: $radius;
       -moz-border-radius: $radius;
        -ms-border-radius: $radius;
            border-radius: $radius;
  }

  .box { @include border-radius(10px); }
```

**.css**

```css
  .box {
    -webkit-border-radius: 10px;
    -moz-border-radius: 10px;
    -ms-border-radius: 10px;
    border-radius: 10px;
  }
```