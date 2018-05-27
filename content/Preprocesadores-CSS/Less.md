# Less

[Less](http://lesscss.org/)

>Es CSS, con solo un poco más.


## Variables

Controle los valores comunes utilizados en una sola ubicación.

**Ejemplo**

```less
  // Variables
  @link-color:        #428bca; // sea blue
  @link-color-hover:  darken(@link-color, 10%);

  // Usage
  a,
  .link {
    color: @link-color;
  }
  a:hover {
    color: @link-color-hover;
  }
  .widget {
    color: #fff;
    background: @link-color;
  }
```

También se pueden usar en otros lugares, como nombres de selector, nombres de propiedades, URL y declaraciones ``@import``.

**.less**

```less
  // Variables
  @my-selector: banner;

  // Usage
  .@{my-selector} {
    font-weight: bold;
    line-height: 40px;
    margin: 0 auto;
  }
```

**.css**

```css
  .banner {
    font-weight: bold;
    line-height: 40px;
    margin: 0 auto;
  }
```

## Mixins

Less es uno de los primeros preprocesadores que son la posibilidad de mezclar selectores. Puede combinar los selectores de clases y los selectores de id

**Ejemplo**

```less
  .a, #b {
    color: red;
  }
  .mixin-class {
    .a();
  }
  .mixin-id {
    #b();
  }

```

Resulta en:

```css
  .a, #b {
    color: red;
  }
  .mixin-class {
    color: red;
  }
  .mixin-id {
    color: red;
  }
```

Si quieres crear un mixin pero no quieres que se compile ese mixin, puedes poner paréntesis después de él.

**.less**

```less
  .my-mixin {
    color: black;
  }
  .my-other-mixin() {
    background: white;
  }
  .class {
    .my-mixin;
    .my-other-mixin;
  }
```

**.css**

```css
  .my-mixin {
    color: black;
  }
  .class {
    color: black;
    background: white;
  }
```

También puede tomar argumentos.

```less
  .border-radius(@radius) {
    -webkit-border-radius: @radius;
       -moz-border-radius: @radius;
            border-radius: @radius;
  }
```

```less
  #header {
    .border-radius(4px);
  }
  .button {
    .border-radius(6px);
  }
```

Los mixins paramétrisados también pueden tener valores predeterminados.

```less
  .border-radius(@radius: 5px) {
    -webkit-border-radius: @radius;
       -moz-border-radius: @radius;
            border-radius: @radius;
  }
```

## Funciones

Less proporciona una variedad de funciones que transforman colores, manipulan cadenas y hacen operaciones matemáticas. 

**Ejemplo**

```less
  @base: #f04615;
  @width: 0.5;

  .class {
    width: percentage(@width); // returns `50%`
    color: saturate(@base, 5%);
    background-color: spin(lighten(@base, 25%), 8);
  }
```

---

## Enlaces de interés

+ [Documentación oficial de Less](http://lesscss.org/)