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
## Funciones

Stylus presenta potentes definiciones de funciones. Las funciones son similares a **mixins**; sin embargo, las funciones pueden retornar un valor.

**.styl**

```styl
  add(a, b)
    a + b

  add2(a, b = a)
    a + b

  body
    padding add(10px, 5)

  section
    padding add2(5px)
```
**Output .css**

```css
  body {
    padding: 15px;
  }

  section {
    padding: 10px; 
  }
```

## Condicionales

Los condicionales proporcionan un flujo de control. Stylus cuenta con condicionales ``if`` que vienen muy útiles a la hora de asegurarnos que algo tiene un valor y que se ejecute algo si eso se cumple.

**.styl**

```styl
  box(x, y, margin = false)
    padding y x
    if margin
      margin y x

  body
    box(5px, 10px, true)
```
**Output .css**

```css
  body{
    padding: 10px 5px;
    margin: 10px 5px;
  }

```

## Iteracion for

Stylus le permite iterar expresiones a través de la estructura ``for / in``, tomando la forma de:

```
  for <val-name> [, <key-name>] in <expression>
```

**.styl**

```styl
  body
  for num in 1 2 3
    foo num
```
**Output .css**

```css
  body {
    foo: 1;
    foo: 2;
    foo: 3;
  }
```