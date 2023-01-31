## Escalabilidad
Propiedad deseable que permite reacciones y adaptarse sin perder calidad o manejar crecimiento continuo o hacerse mas grande sin perder calidad.
### Dimensiones
- Tamanio: agregar recursos y usuarios
- Ubicacion: que usuario y recursos estan mas lejos de otros
- Administracion: facil de usar y manejar sin importa cuantos lo usen
### Tipos
- Vertical: Agregar mas recursos a un nodo "ram, disco duro, procesador"
- Horizontal: Agregar mas nodos
### Escabilidad desde el Software
Aplicacion escalable cuando se agrega recursos rendmiento crece de manera proporcional
- Se evita cuello de botellas con rendimientos con datos jerarquicos con mejor tiempo de acceso
- Uso de software eficiente 
- Patrones de diseno y codigo facil para manejar mejor conexion, hilos
- Usar cache y consistencia eventual, replicacion, load balancer
### Cache
- Forma especial de replicacion
- Copia de recursos de uso general del usuario
### Replicacion con escalado
- Cuando haya una actualizacion sea atomica o transaccion
- Atomicidad necesita gran numero de replicas distribuidad por la red, generado latencia
- Sincronizacion de replicas problema
- Para matener copias actualizdas require rendimiento
- Solucion relajar o bajar restricciones de consistencia
- Evitar sincronizacion globales para rendimiento
### Data-centric consistency
- Consistencia basado en lectura y escritura de datos compartidos
- Contrato entre processos y almacenamiento
- Si se acepta las reglas el almacenamiento funciona
- Proceso de lectura espera la ultima operacion de escritura
- Se define modelo que restringe valores de operacion
### Continuos consistency
- Inconsistencia"
	- Desviacion en valores numericos entre replicas
	- Desviacion por obsolencia de replicacs
	- Desviacion por orden en operaciones de actualizacion
### Desviacion numerica
- Rangos de incogerencia son usados para numeros
	- "Stock de precios donde dos copias no pueden tener desviacion de 0.02 ctvs"
### Desvicacion por obsolecencia
- Se ve cuando fue la ultima vez que se actualizo
- Se puede tolerar datos sin actualizaron en un tiempo x
### Desviacion por actualizaciones
- Orden de actualizacion diferentes para replicas
- aplicaciones en diferente orden para las replicas
### Unidad de Incosistencia
- CONIT es la unidad de incosistencia