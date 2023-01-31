Bloque de contruccion de aplicaciones angular que poseen:
- HTML template para declarar lo que se renderiza en la pagina
- Clase Typescript que define el componente y la logica
- Selector CSS que define como sera llamado el componente
- Estilo CSS que es aplicado al template

## Cracion de Componente
--- 
### Angular CLI
`ng generate componente <component-name>`, crea un archivo para el componente (.ts), template (.html), estilo (.css) y testeo (.spec.ts).

## Manualmente
Carpeta del componente codificar: 

```
import {Componente} from '@angular/core'; // Importacion de modulo de componentes 

@Componente({ // Decorador para clase actual del compoente
	selector: 'app-component', // Nombre de llamado del compoenent,
	templateUrl: './dir', // Direccion de template file
	styleUrls: ['./dir-1', './dir-2'] // Direccion de css styles
})
```

### Selector CSS
El selector indica a Angular instanciar el componente siempre que encuentre la etiqueta que le corresponde en una plantilla HTML.

### Template Component
Indica como renderizar el componente en la aplicacion, por medio de una referencia de archivo o en el componente, se puede usar solo una propiedad template o templateUrl.
```
templateUrl: './component-overview.component.html',
----------------------------------------------------------
template: `
	<h1>Hello World!</h1>
<p>This template definition spans multiple lines.</p>
`
```

### Styles Components
Estilos usados por el template, se puede asignar al igual que el template en el componente ya sea con archivo o internamente
```
styleUrls: ['./dir']
--------------------------------------------
styles: ['h1 {text-align: center;}']
```