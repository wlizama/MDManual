# ReactJS con Redux

Apuntes relacionados a Redux dentro de ReactJS.

## Definición básica

De manera sencilla se puede definir como una libreria que facilita la conección entre diferentes fuentes y/o entornos que cumplen un mismo objetivo.

Redux se basa en 3 principios: 

**1- Una sola fuente de datos:** El estado de la información se almacena en un árbol de objetos dentro de una única **STORE**, esto facilita la depuración y el desarrollo rápido.

**2- El estado es solo de lectura:** La única forma de cambiar el estado es enviando una señal al **STORE**. Esta señal es un (**ACTION**).

**3- Las mutaciones se escriben como funciones puras:** El responsable de especificar de como cambiará el estado por medio de las acciones son los **REDUCCERS**se son acciones puras que reciben el estado anterior y la acción a realizar devolviendo un nuevo estado, en lugar de modificarla.

## STATE

Es la mínima representación de los datos en nuestra aplicación.

## ACTIONS

Los estados de una aplicación solo cambiarán si se dispara un **ACTION**. Una acción es un objeto plano que describe un cambio, cada **ACTION** debe tener siempre una propiedad diferente de `undefined` y en cada aplicación debe existir la definición de sus propios **ACTIONS** para los cambios de estado en sus datos.

Redux no entiende otros tipos de acción que un objeto simple. Si desea mover la lógica asincrónica de React a Redux y poder devolver funciones en lugar de objetos simples, debe usar un middleware personalizado. Con [Redux Thunk](https://github.com/reduxjs/redux-thunk) se puede devolver funciones de creadores de acciones, no solo objetos. Puede hacer un trabajo asincrónico dentro de sus acciones y disparar otras acciones en respuesta a llamadas AJAX..

## REDUCERS

Es una función pura que tiene toda la aplicación Redux y devuelve un nuevo estado de los datos pasando como párametros el estado (**STATE**) previo y la acción (**ACTION**) a ejecutar. Si se pasa una acción que no esta definida devolveremos el mismo estado que recibió.
Los reductores deben mantenerse delgados y limpios. Un reductor no es un buen lugar para la lógica asincrónica.

```js
// Ejemplo de Reducer
// nunca se cambia el estado, devuelve 0 (cero) si el estado es undefined
// devolvemos el nuevo estado si conoceomos la acción

const myReducer(state = 0, action) => {
    switch(action.type) {
        case: 'SUMAR':
            return state + 1
        case:  'RESTAR':
            return state - 1
        default: 
            return state
    }
}

// pasamos acciones al reducer
myReducer(0, { type: 'SUMAR' })  // -> state = 1
myReducer(1, { type: 'RESTAR' }) // -> state = 0
```

## STORE

Un store contiene los 3 principios de Redux será el centro de la aplicación ya que con el se conoce el estado de la aplicación y nos permitirá ejecutar acciones para modificar el estado.

Para poder crear un store necesitamos pasarle un **REDUCER** con la lógica de los cambios.

El **STORE** tiene 3 métodos importantes:

- _getState()_: Devuelve es state del actual **STORE**.

- _dispatch()_: Dispara **ACTIONS** para cambiar el **STATE**.

- _subscribe()_: Es un callback que será llamado con cada dispatch haciendo que tengamos disponible actualizado el método `getState()`, escucha los cambios de cada estado.

**Funciones Puras**

Una función pura recibe argumentos pero no los modifica dentro de su proceso, su comportamiento es facilmente testeable.

```js
// opera con el argumento pero no lo modifica
function doblar(nm) {
    return num * 2
}

// retorna un nuevo listado sin modificar el de ingreso
function doblarLista(lst) {
    return lst.map(doblar)
}
```

**Funcion impura**

Realizan modificaciones directas sobres los argumentos que recibe.

```js
// realiza modificación de sobreescrita de los valores de argumento de entrada
function doblarLista(lst) {
    for(var i = 0; i < lst.items: i++) {
        lst[i] = doblar(lst[i])
    }
}
```

## Redux Saga

[Redux Saga](https://github.com/redux-saga/redux-saga) es un middleware de Redux para gestionar los efectos secundarios. Con redux saga puede tener un hilo separado en su aplicación para tratar acciones impuras: llamadas a la API, acceso al almacenamiento y más.

Es diferente de una acción asíncrona en términos de sintaxis y organización del código. Con [Redux Thunk](https://github.com/reduxjs/redux-thunk) puedes poner una llamada API directamente dentro de un creador de acciones, mientras que en redux saga puedes tener una separación clara entre lógica síncrona y asíncrona. Y esa lógica estará totalmente separada de su código Redux.


En redux saga podría alojar en un solo archivo que contiene:

- a **worker function**

- a **watcher function**

**Watcher function** es una [función generadora](http://es6-features.org/#GeneratorFunctionIteratorProtocol) que observa cada acción que nos interesa. En respuesta a esa acción, el **watcher function** llamará a un **worker function**, que es otra función generadora para realizar la llamada API real.


## Más info

- [Redux Documentación (español)](https://es.redux.js.org/)

- [Blog Redux app de ejemplo (inglés)](https://www.valentinog.com/blog/redux/)

- [Redux Toolkit Documentation](https://redux-toolkit.js.org/introduction/quick-start)

- [Redux Saga](https://github.com/redux-saga/redux-saga)

- [Ducks Modular Redux 🦆](https://github.com/erikras/ducks-modular-redux)