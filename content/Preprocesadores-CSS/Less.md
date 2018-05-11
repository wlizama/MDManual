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