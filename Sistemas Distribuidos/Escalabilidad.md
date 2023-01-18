## Escabilidad y Costo
- Tendencia lineal de escalamiento depende del contexto
	- Aumento de solicitudes proporcional al aumento de tiempo de repuesto no es escalabildad "directamente propocional"
	- Aumento de solicitudes con mismo tiempo de repuesta "sin relacion".

### Consideraciones de escalabildad

Configuraciones simples, de bajo costo y tiempo..
- Escalabilidad horizontal, aumento de servidor con maquina virtual (30m)
- Reconfiguracion de sistemas con ejecucion de varios sevidores paralelos.

### Dificultades
- Base de datos menos receptivas con mas peticiones por segundos (15h)
- Servidor web genera mayor cantidad de contenido dinamico - "Refactorizar para hacer codigo mas eficiente, reducion tiempo de procesamiento".
- Carga de solicitudes provoca puntos calientes al tener intentar leer y actualizar el mismo dato - "Rehacer esquema y recarga de datos de la base y cambiar codigo para el acceso"
- Codigo simple (Mejor desarrollo) no es escalable requiere reescritura completa (10000h).

Costos de recursos y esfuerzos estan estrechamente ligados a escalabildad.
Sistema debe estar pensado para ser escalado sino puede tener costos de escalabildad altos.
Se debe emplear arquitecturas, mecanismos y tecnologias escalables desde el comienzo para reducir costos.

### Sistemas de hiperescala

Sistemas de software que crecen a medida que los costos lo hacen.
“ _Los sistemas de hiperescala exhiben un crecimiento exponencial en las capacidades computacionales y de almacenamiento, al mismo tiempo que exhiben tasas de crecimiento lineal en los costos de los recursos necesarios para construir, operar, respaldar y evolucionar los recursos de software y hardware requeridos_ ”.

- Se debe definir un sistema escalable en la arquitectura, donde se pueda aumentar la capacidad del sistema, por replicaciones, optimizacion de rendmiento de componentes