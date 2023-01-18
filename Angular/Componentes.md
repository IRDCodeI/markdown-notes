Bloques de codigo que puede tener una pagina web y que son reutilizables, y que ademas estructuran una pagina web.
- Generar Componentes `ng generate 'g' components 'c' components/header 'dir/name' --no-spec 'no test file'`
- Cada componente posee archivos o codigo de html, css y ts

## Aplicaciones Clave
- **{{}}**: Interpolacion de Javascript/Typescript en HTML
- **(click)**: Llamado de eventos
- **< ... ngFor="let num of arr"">{num}**: Interpolacion de datos con directiva For-Angular
- **"add()"**: Llamada de funciones declaradas
- **@Decorador**: Opciones extras agregadas a posteriori en clases
- **constructor()**: Seccion que se ejecuta al construir la clase
- **ngOnInit()**: Seccion que se ejecuta
- **ngIf**: Directiva para html 
- ngContainer: Componente para agrupar contenido
- ng-template name:  Estructura que permite asignacion de un nombre

## Interfaces, Enumeraciones y Casting
---
### Interfaces
Definiciones de objetos, osea es la estructura que poseera un objeto

```
export interface Usuario{
	ID: number,
	Nombre: string,
	Apellidos: string,
	Nick: string,
	Email: string,
	Clave: string
}

user:Usuario = { // Campos obligatorios de objeto basado en interfaz
	ID: 23, 
	Nombre: "Stalin",
	Apelldios: "David",
	Email: "rdcode@gmail.com",
	Nick: "RDCode",
	Clave: "1234"
}
```
### Enumeraciones
Lista de posibilidades

```
export enum UserType{
	Administrador,
	Cliente,
	Tecnico
}

user:Usuario = { 
	ID: 23, 
	Nombre: "Stalin",
	Apelldios: "David",
	Email: "rdcode@gmail.com",
	Nick: "RDCode",
	Clave: "1234",
	Tipo: UserType.Administrador
}

users:Usuario[] = [
	{ 
		ID: 23, 
		Nombre: "Stalin",
		Apelldios: "David",
		Email: "rdcode@gmail.com",
		Nick: "RDCode",
		Clave: "1234",
		Tipo: UserType.Administrador
	},
	{ 
	ID: 23, 
	Nombre: "Stalin",
	Apelldios: "David",
	Email: "rdcode@gmail.com",
	Nick: "RDCode",
	Clave: "1234",
	Tipo: UserType.Tenico
	}
]
```

### Casting
Permite transforar tipo de dato object a otro tipo de dato como interfaz, nos ayuda cuando solicitamos datos desde una API, nos dara un dato JSON pero si no definimos la interfaz de dicho objeto no tendremos sugerencias del editor.

```
user:Usuario = <Usuario>{ // Casting<> 
	ID: 23, 
	Nombre: "Stalin",
	Apelldios: "David",
	Email: "rdcode@gmail.com",
	Nick: "RDCode",
	Clave: "1234",
	Tipo: UserType.Administrador
}
```

### Atributos, Eventos y ngModel
