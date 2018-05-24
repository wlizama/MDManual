# ReactJS

Es una librería de JavaScript para construir interfaces de usuarios.

## Particularidades de ReactJS
+ **Declarativo:** Es muy sencillo escribir interfaces y poderlas leer.

+ **Basado en componentes**

## Existen tres tipos de componentes
+ **Funcional**
+ **Puro**
+ **Normal o de Estado**

## Ciclo de vida de los componentes
+ **Montado:** El momento en que el componente entra en escena.
  + **Constructor:** método llamado antes de que el componente sea montado (componente aun no se ve).
    + Podemos iniciar el estado.
    + Enlazar eventos (bind).
    + Es el primer metodo que se llama al instanciar un componente.

  + **componentWillMount:** método llamado inmediatamente antes de que el componente se vaya a montar (componente aun no se ve).
    + Podemos hacer un setState()
    + No hacer llamados a un API o suscripción a eventos.
  
  + **Render:** método que contiene todos los elementos a renderizar (estructura del componente).
    + Contiene JSX en el return.
    + Puedes calcular propiedades `nCompleto = name + lastName`.

  + **componentDidMount:** Método llamado luego de montarse el componente (el componente ya esta en la pantalla).
    + Solo se lanza una vez.
    + Enlazar (bind) de eventos.
    + Es el primer método que se llama al instanciar un componente.
    + Aqui podemos utilizar APIs (Navegador o Datos Externos).

+ **Actualización**
  + **componentWillReceiveProps:** método llamado al recibir nuevas propiedades que sirve para actualizar el estado con base a las nuevas propiedades.
  + **shouldComponentUpdate:** método que condiciona si el componente se debe volver a renderizar, es utilizado para optimizar el rendimiento.
  + **componentWillUpdate:** método llamado antes de re-renderizar un componente, es utilizado para optimizar el rendimiento.
  + **Render:** método que realiza el re-render.
  + **componentDidUpdate:** método llamado luego del re-render.

+ **Desmontado**
  + **componentWillUnmount:** método llamado antes de que el componente sea retirado de la aplicación.

+ **Manejo de Errores**
  + **componentDidCatch:** método llamado cuando ocurre un error al renderizar el componente, el manejo de errores solamente ocurre en componentes hijos.

## Componentes puros y funcionales en ReactJS
**PureComponent:** tiene el método _shouldComponentUpdate_ ya asignado (por defecto), si a este componente no se le actualizan las propiedades, no tenemos que validar a mano con _shouldComponentUpdate_, _PureComponent_ lo hace por nosotros, es decir; si recibe nuevas propiedades pero son las que ya teniamos, no se re-renderiza.

```jsx
import React, { PureComponent } from 'react';

class Playlist extends PureComponent{
  render() {
    <Componente />
    }
}
```

**Componente Funcional:** Es una función la cual solo retorna el JSX de nuestro componente (renderiza UI), es mas sencillo, mas fácil de probar y este componente no tiene ciclo de vida.

```jsx
import React from 'react';

function Playlist(props) {
  return <Componentetitle={props.title} />
}
```

## Smart Components and Dumb Components
**Presentacional** Cómo se ve

+ Puede contener smart components u otros componentes de UI.
+ Permiten composición con `props.children`.
+ No depeden del resto de la aplicación.
+ No especifica cómo los datos son cargados o mutados.
+ Recibe datos y callbacks solo con propiedades.
+ Rara vez tienen su propio estado.
+ Están escritos como componentes funcionales a menos que necesiten mejoras de performance. Sólo pueden ser Componentes funcionales o Pure Components.

**Containers** Qué hace

+ Concetrado en el funcionamiento de la aplicación.
+ Contienen componentes de UI u otros containers.
+ No tienen estilos.
+ Proveen de datos a componentes de UI u otros contenedores.
+ Proveen de callbacks a la UI.
+ Normalmente tienen estado.
+ Llaman acciones.
+ Generados por higher order components.


**Portales** es la manera en la que podemos renderizar componentes fuera del contenedor principal de la aplicación.

**Referencias** Las referencias nos permite almacenar en react un elemento HTML

_value_: No permite editar el input al menos que se envie el valor mediante props.

_defaultValue_: permite editar el input

---

## Enlaces de interés

+ [Documentación oficial ReactJS](https://reactjs.org/docs)