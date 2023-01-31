Plataforma de desarrollo construido en Typescript, incluye:
- Framework de componenetes para apps escalables
- Coleccion de librerias que cubren, routing, forms, http request, etc.
- Suite de herramientas para desarrollar, construir y testear el codigo.
- Framework para construir SPA (Single Page Application)
- Construccion de bloques basica de Angular son los componente que se organizan en `NgModules`.
	- NgModules collecion de set de funcionalidades relacionadas al codigo.

## Conceptos Escenciales

### **Componentes**
---
Bloques que componen la aplicacion, los cuales incluyen: *Clase Typescript con un Decorador (@Component ), plantilla HTML y estilos CSS.*

Ademas posee una encapsulacion fuerte y estructura senciila.
```
@Component({
	selector: 'hello-world',
	templateURL: './dir' or template: `<h1>Hello World</h1>`
	stylesURL: ['./dir-1','./dir-2']
})
```

```
<hello-world></hello-world>
```

### **Templates**
---
Plantilla HTML que se declara con el componente, pero que en Angular se extiende dicha sintaxis HTML, permitiendo agregar valores dinamicos basado en reactividad (Actualiza el DOM cuando el estado cambia).

```
<p>{{message}}</p>
```

```
...
export class HelloWorld {
	message = 'Hello World!';
}
```

Algunas de las aplicaciones mas comunes en componentes son: 

- **Interpolacion**: Permite agregar valores dinamicos mediante el uso de doble llaves `{{}}`
```
<p>{{message}}</p>
```
- **Binding de propiedades**: Permite establecer valores de propiedades y atributos de HTML por medio del uso de corchete `[]`
```
<p 
	[id]="sayHelloId" 
	[style.color]="fontColor"> 
	You can set my color in the component! 
</p>
```
- **Eventos**: Permite vincular un event listener a una funcion que actuara como handler evet por medio del uso de parentesis
```
<button 
	type="button" 
	[disabled]="canClick" 
	(click)="sayMessage()"> 
	Trigger alert message 
</button
```

### **Inyeccion de Dependencia**
---
Patron de diseño que permite declara las dependencias de una clase Typescript sin preocuparse por la instansacion de la misma.

```
@Injectable({provideIN: 'root'})
```

```
...
constructor(private logger: Logger){}
...
```

### **Angular CLI**
---
Herramienta de consola que permite automatizar tareas recurrentes que se hacen en el desarrallo de aplicaciones Angular
- **ng build**: Compilar aplicacion dentro de un directorio de salida
- **ng serve**: Correr un servidor de aplicacion con hot reload
	- -o: Abre automaticamente el navegador
- **ng generate**: Generar o modificar archivos basado en esquemas
- **ng test**: Ejecutar unit test en un proyecto
- **ng e2e**: Correr un servidor de aplicacion angular con ent-to-end test

### Librerias Angular
---
Librerias de uso comun para desarrollo de aplicaciones:
- Angular Router: Navegacion y Routing para componentes de angular, soporta lazy-loading, nested routes, custom path, matching, ...
- Angular Forms: Sistema para creacion y validacion de formularios.
- Angular HttpClient: Comunicacion cliente servidor
- Angular Animation: Manejador de animacion basado en aplicaciones estaticas
- Angular PWA: Herramientas para desarrollar PWA incluyendo service worker y Web applicaciont manifest