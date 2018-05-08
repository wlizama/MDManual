# Stylus

Stylus es un pre-procesador de css. Los archivos **.styl** se compila para luego guardarlo en un archivo _CSS_. Por lo tanto se traduce del lenguaje de Stylus al lenguaje de CSS.

Stylus trabaja con **NodeJS**.

## Sintaxis

+ Su sintaxis es anidada.

+ En Stylus no es necesario usar los brackets ``{}``y ``;``

## Anidaciones

Con el uso de ``&`` hacemos referencia al nombre del elemento padre

```styl
  .pseudo-element
    width 300px

    &:before
      content ':)'
    
    .ie-8 &
      &:before
        content ':('
```

## Variables

Estas nos permiten controlar un entorno. Esto quiere decir que podemos cambiar muchas cosas a través de muchas variables.

Podemos asignar expresiones a variables y usarlas en nuestra hoja de estilos:

**.styl**

```styl
  font-size = 14px

 body
   font font-size Arial, sans-serif
```

**Output .css**

```styl
  body {
   font: 14px Arial, sans-serif;
  }
```

## Mixins

Los mixins son declarados a través de nombres. Es importante que siempre añadamos el prefijo _mixin_ para poderlos identificar.

**.styl**

```styl
  /* variable declarada en el archivo _variables.styl */

  page-max-width= 1024px

  mixin-max-width(width=page-max-width)
    max-width:width
    margin-left:auto
    margin-right:auto

  /* aqui toma el valor por defecto */
  .container
    mixin-max-width()

  /* Aplicando el mixin con valor custom */
  .section
    mixin-max-width(90%)
```

**Output .css**

```css
  .container {
    max-width: 1024px;
    margin-left: auto;
    margin-right: auto;
  }

  .section {
    max-width: 90%;
    margin-left: auto;
    margin-right: auto;
  }
```