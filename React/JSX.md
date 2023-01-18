**React** bilbioteca de javascript para creacion de interfaces de usuario.

___
## JSX

```
const element = <h1>Hello, world</h1>
```

- Extension de sintaxis Javascript para describir la interfaz de usuario.
- JSX produce **elementos** de React
- *Renderizado esta unido a la logica de la interfaz de usuario*: Manejo de eventos, cambio de estado en el tiempo y presentacion de datos para visualizacion.
- **Separa intereses**: Cada seccion se enfoca a un problema en espeficico "componentes".
- JSX es Javascript por lo que se usa camelCase.
- Etiquetas vacia se puede cerrar con "/>"

___
### Expresiones JSX

```
const name = "Stalin"
const element = <h1>Hello, {name}</h1>
```
- Se puede agergar cualquier expresion **Javascript** en las llaves JSX "{}" como *2+2, user.firstName o formatName(user)*.

```
function formatName(user) {
  return user.firstName + ' ' + user.lastName;
}

const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};

const element = (
  <h1>
    Hello, {formatName(user)}!  </h1>
);
```

- Compilacion convierte expresiones JSX en llamadas a funciones Javascript regulares.
	- Permite usar JSX dentro de declaraciones *if* y *for*, dar varibales, aceptar como argumento.

```
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;  
  }
  return <h1>Hello, Stranger.</h1>;}
}
```

___
### Atributos JSX
Se puede usar strings para atributos o por medio de expresion Javascript pero **solo una de las dos a la vez**.
```
const element = <a href="https://www.reactjs.org"> link </a>;
const element = <img src={user.avatarUrl}></img>;
```

___
### Hijos con JSX

Etiquetas Javascript pueden tener hijos:
```
const element = (
  <div>
    <h1>Hello!</h1>
    <h2>Good to see you here.</h2>
  </div>
);
```

___
### JSX contra inyeccion.

Seguro insertar datos ingresados por el usuario ya que escapa a cualquier valor insertado en JSX antes de renderizarlo, evitando asi XSS (cross-site-scripting).
```
const title = response.potentiallyMaliciousInput;
// Esto es seguro:
const element = <h1>{title}</h1>;
```

___
### JSX representa objetos

JSX se compila a llamadas de React.createElement() donde create "Elementos de React", los cuales son como descriptores de lo que se quiere ver, donde React lee los objetos y los usa para construir el DOM.
```
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```

```
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

Se crea este objeto:
```
// Nota: Esta estructura está simplificada
const element = {
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello, world!'
  }
};
```