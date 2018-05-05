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