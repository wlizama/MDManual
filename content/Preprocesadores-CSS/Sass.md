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

**Output .css**

```css
  .box {
    -webkit-border-radius: 10px;
    -moz-border-radius: 10px;
    -ms-border-radius: 10px;
    border-radius: 10px;
  }
```

### Variable Scope and Content Blocks

Una de las características que tienen los mixins es la directiva ``@content``. Esta nos permite incluir un bloque de contenido dentro de un mixin.

**.Scss**

```scss
  $color: white;
  @mixin colors($color: blue) {
    background-color: $color;
    @content;
    border-color: $color;
  }
  .colors {
    @include colors { color: $color; }
  }
```

**Output .css**

```css
  .colors {
    background-color: blue;
    color: white;
    border-color: blue;
  }
```

## Extend

Esta es una de las características más útiles de Sass. El uso de **@extend** le permite compartir un conjunto de propiedades CSS de un selector a otro. Ayuda a mantener tu Sass muy seco. Es un tipo especial de clase que solo se imprime cuando se extiende, y puede ayudar a mantener su CSS compilado ordenado y limpio.

**.Scss**

```scss
  // This CSS won't print because %equal-heights is never extended.
  %equal-heights {
    display: flex;
    flex-wrap: wrap;
  }

  // This CSS will print because %message-shared is extended.
  %message-shared {
    border: 1px solid #ccc;
    padding: 10px;
    color: #333;
  }

  .message {
    @extend %message-shared;
  }

  .success {
    @extend %message-shared;
    border-color: green;
  }

  .error {
    @extend %message-shared;
    border-color: red;
  }

  .warning {
    @extend %message-shared;
    border-color: yellow;
  }
```

**Output .css**

```css
  .message, .success, .error, .warning {
    border: 1px solid #cccccc;
    padding: 10px;
    color: #333;
  }

  .success {
    border-color: green;
  }

  .error {
    border-color: red;
  }

  .warning {
    border-color: yellow;
  }
```

## Funciones

_Sass_ define algunas funciones útiles que se llaman usando la sintaxis normal de la función CSS:

**.Scss**

```scss
  p {
    color: hsl(0, 100%, 50%);
  }
```

**Output .css**

```css
  p {
  color: #ff0000; }
```

Consulte esta (página)[https://sass-lang.com/documentation/Sass/Script/Functions.html] para obtener una lista completa de las funciones disponibles.

## @each

La directiva ``@each`` tiene la forma ``@each $var in <list or map>`` donde ``$var`` va tomando cada valor durante la iteración de ``<list or map>``. Ejemplo:

**.Scss**

```scss
  @each $animal in puma, sea-slug, egret, salamander {
    .#{$animal}-icon {
      background-image: url('/images/#{$animal}.png');
    }
  }
```

**Output .css**

```css
  .puma-icon {
    background-image: url('/images/puma.png'); }
  .sea-slug-icon {
    background-image: url('/images/sea-slug.png'); }
  .egret-icon {
    background-image: url('/images/egret.png'); }
  .salamander-icon {
    background-image: url('/images/salamander.png'); }
```

## @for

La diferencia de  ``@for`` con ``@each`` es que para cada repetición se usa una variable contador para ajustar la salida. ``@for`` se puede escribir de 2 formas ``@for $var from <start> through <end>`` y ``@for $var from <start> to <end>``. Cuando ``<start>`` es mayor que ``<end>``, el contador disminuirá en lugar de incrementarse.

**.Scss**

```scss
  @for $i from 1 through 3 {
    .item-#{$i} { width: 2em * $i; }
  }
```

**Output .css**

```css
  .item-1 {
    width: 2em; }
  .item-2 {
    width: 4em; }
  .item-3 {
    width: 6em; }
```