# ReactJS con Redux

Apuntes relacionados a Redux dentro de ReactJS.

## Definición básica

De manera sencilla se puede definir como una libreria que facilita la conección entre diferentes fuentes y/o entornos que cumplen un mismo objetivo.

Redux se basa en 3 principios: 

**1- Una sola fuente de datos:** El estado de la información se almacena en un árbol de objetos dentro de una única **STORE**, esto facilita la depuración y el desarrollo rápido.

**2- El estado es solo de lectura:** Solo podemos cambiar los estados por medio de **ACTIONS**.

**3- Las mutaciones se escriben como funciones puras:** El responsable de especificar de como cambiará el estado por medio de las acciones son los **REDUCCERS**se son acciones puras que reciben el estado anterior y la acción a realizar devolviendo un nuevo estado, en lugar de modificarla.

## STATE

Es la mínima representación de los datos en nuestra aplicación.

## ACTIONS

Los estados de una aplicación solo cambiarán si se dispara un **ACTION**. Una acción es un objeto plano que describe un cambio, cada **ACTION** debe tener siempre una propiedad diferente de `undefined` y en cada aplicación debe existir la definición de sus propios **ACTIONS** para los cambios de estado en sus datos.

## REDUCERS

Es una función pura que tiene toda la aplicación Redux y devuelve un nuevo estado de los datos pasando como párametros el estado (**STATE**) previo y la acción (**ACTION**) a ejecutar. Si se pasa una acción que no esta definida devolveremos el mismo estado que recibió.

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

## Más info

- [Redux Documentación español](https://es.redux.js.org/)