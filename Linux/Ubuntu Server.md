
## Comandos Basicos

Metodo de Conexion al servidor (SSH): 

- Sevidores Linux solo permiten acceso **root** por medio de la consola
  
  - Se aplica el comando `sudo su -` para crear una nueva sesion con otro usuario sin cerrar la conexion anterior.
  
  - `lastlog -u "username"`: Permite saber la ultima sesion del usuario.

- Comando de exploracion para concer estado del disco duro o file-systems `df -h` 

- Capacidad de memoria ram en el servidor `free -m` 

- Monitoreo de procesos en el servidor `top` 

## **Vulnerabilidades Servidores**

Se debe poseer un usuario que no sea root o no tenga permisos, por lo que se debe iniciar con un **usuario normal** sin nivel de administrador.

- `useradd -c "user-name" -g  "user-group" -d "path-dir" -m -s "bash-dir name-user"`

- `passwd "username"` 
