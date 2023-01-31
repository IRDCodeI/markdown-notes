
El cilo de vida de un componente empieza con las instancia de la clase y el renderizado en la vista junto con sus vistas hijas, posterior continua en la detecion de cambios en propiedades vicnuladoas actualizando las vista e instancia. Finaliza con la destruccion de la instancia y eliminacion del renderizado en el DOM.
- Directivas tienen un ciclo de vida similiar por que crean, actualizan y destruyen instancias.
- Lifecycle hook methods permiten usar estos eventos para realizar diferentes acciones.

## Respuesta a eventos de ciclo de vida
---

Se hace uso de las *Interfaces de lifecycle hooks* de la libreria `core` . Permitiendo actuar en el momento adecuado, cuando se crean, actualizan o destruyen instancias.
- Cada interfaz (ng) define su metodo (ngOnInit).

```
export class PeekAbooDirective implements OnInit {
	ngOnInit() P
	this.logIt('OnInit');
}
```

### Secuencia de eventos de ciclo de vida

|Metodo|Proposito|
|---|---|
|ngOnChanges()|Responder cuando se establece o restablece datos vinculados a propiedades|
|ngOnInit()|Inicializar despues de renderizar por primera vez datos vinculados a propiedades |
|ngDoCheck()|Detectar y actuar en cambios que no se detecten por Angular|
|ngAfterContentInit()|Actuar despues de mostrar contenido en la vista del componente|
|ngAfterContentChecked()|Responder despues de que se verifique el contenido proyectado|
|ngAfterViewInit()|Cuando se inicialice las vistas del compoentnes|
|ngAfterViewChecked()|Cuando se verifique las vistas del componente|
|ngOnDestroy()|Limpieza antes de destruir el compoennte, anular subscribe, observable, controlador, etc|

![life_cycle](https://lh4.googleusercontent.com/jqfQIpB5PJcoOn8n9fMW466u69Fs-kS4pKMzr3nKPmLRj_T730J9MB3kBRfaI9A_T3T5PFYOsjL0lSJkl_NifKbzhOJgkZKU5bQmiZhXwz8Tcu_uT6rsSlA8gFF5hl-YBRybh0RA)
