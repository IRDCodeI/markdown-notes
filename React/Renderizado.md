Elementos son bloques de objetos planos, con creacion de bajo costo que forman la aplicacion y donde **React DOM** (Virtual DOM) se encarga de actulizar el DOM.

```
const element = <h1>Hello, world</h1>;
```

## Renderizado en el DOM

La renderizacion de elementos parten de un nodo raiz (**root**) el cual es manejado por el React DOM y aqui es donde los elementos o componentes se van a ir insertando. El proceso es pasar el elemento del DOM `ReactDOM.createRoot()` y posterior renderizar dicho elemento `.render()`.

**Elemento**:
```
<div id='root'></div>
```
**Nodo raiz**:
```
const root = ReactDOM.createRoot(
	document.getElementById('root')
);

const element = <h1>Hello World!</h1> --> JSX

root.render(element); --> Render
```

## Actualizacion de elemento renderizado

Elementos en React son **inmutables**, por lo que sus valores no se pueden cambiar una vez sea creado ya que representa la interfaz en cierto punto del tiempo. Teniendo esto presente lo unico que cambia **es el contenido** del elemento.

Dicha actualizacion de contenido es por medio de la compracion de elemento e hijos con el elemento anterior, actualizando solo lo necesario del DOM.

*Interfaz de usuario en un momento dado y no cambiarlo todo el tiempo*.

```
const root = ReactDOM.createRoot(
  document.getElementById('root')
);

function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  root.render(element);}

setInterval(tick, 1000);
```