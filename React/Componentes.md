Son piezas independientes, reutilizables y aisladas de codigo, las cuales aceptan entradas **"props"** y retornan elementos de React, diciendo lo que se debe mostrar en pantalla.

## Componente Funcional

Se declara por medio de una funcion "componente" la cual acepta solo un argumento de objeto "props (propiedades)" con datos y retorna un elemento React. Se lo relaciona con una funcion Javascript.

```
function Welcome(props) {
	return <h1>Hello, {props.name}</h1>
}
```

## Componente de Clase 

Se lo declara por medio de una clase de ES6

```
class Welcome extends React.Component {
	render() {
		return <h1>Hello, {this.props.name} </h1>
	}
}
```

## Renderizado de Componente

Se trata del renderizado de elementos/componentes definidos por el usuario, donde React ve el elemento como una representacion de dicho componente definido, con atributos JSX e hijos en pocas es un objeto.

```
// Componentes siempre con mayuscula para diferenciar de elementos JSX

function Welcome(props) {  return <h1>Hello, {props.name}</h1>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
const element = <Welcome name="Sara" />;root.render(element);
```

## Composicion de componentes

