## Arquitectura de Twitter

### Servicio de Tweets
- Tweets en usuarios: Recibir, reenviar, linea de tiempo y busqueda
- Almacenamiento de informacion: Usuario, cantidad de tweets y gustos
- Datos: Datos distribuidos, cache en memoria 

### Identificacion unica de Tweet
- Funcion postTweet() genera UI por medio de RPC "Servidor de aplicaciones"
- ID de Tweet se guarda en cache y en base de datos "CQRS"

### Escalar Tweets
- Escalamiento para fragmento de ID de tweets y ID Usario "Shareded Services"

## Servicio de grafico social
- Seguimiento entre usuarios "Grafo" "RCP" ubicado en servidores de aplicaciones
- Servicios para manejo de acciones (Eliminar usuarios, linea de tiempo, ...) por medio de "API (Asincronico)" "RPC"

### Servicio de linea de tiempo del usuario
- Serivicio de historial de tweets realizados en forma descendente "RPC" "Cache" 
- Lista enlazada "Nuevo tweet al principio" "1000 tweets y cada nuevo tweet elimina el ultimo cuando se pasa el limite"

### Servicio de Abanico (Fanout) "Revisar"
- Reenvia nuevos tweets a la busqueda cuando hay nuevos componentes/microservicios "Eventos - SAGA"
- Colas distribuidas "Mensaje en cola" "Servidor de Colas" "Tarea Asincrona"

### Servicio de linea de tiempo en casa
- Linea tiempo de inicio 
- Tweets de otros usuarios en orden descendente 
- Elimina el tweet mas antiguo cuando pasa K valor
- CQRS

### Servicio de busqueda
- Fanout pasa el tweet a la busqueda
- "Motor de ingestion": Separa el tweet en palabras clave basado en lista de configuracion o base de datos
- Derivacion transforma palabras en su raiz, buscando en un tabla siempre que este dicha palabra almacenada
- Indice de la palabra almacenada para buscar
- Crea indice invertido que almacena indice de asignacion de terminos del contenido
- Blender: Terminos de busqueda, luego ingestion y derivada 

### Fotos y videos
- NoSQL
- Fotos "Sistema de archivos"
