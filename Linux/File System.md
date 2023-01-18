
Sistemas de archivos, subcapa que controla la posicion de los datos almacenados. **"Mecanismos de gestion de archivos para ser nombrados, recuperados, etc"** 

- *Datos del Usuario*: Informacion del usuario, credenciales, actividades, etc

- *Metadatos*: Informacion de archivos creados por usuarios.

**Tipos de FS**: EXT2, EXT3, EXT4, ...

## Directorios de Archivos

Permiten gestionar la informacion

- /bin: Comandos del sistema "ls"

- /dev: Ubicacion de los sistemas montados

- /etc: Paquetes instalados y scripts de los mismos

- /boot: Archivos para iniciar y cargar el sistema 

- /home: Carpeta de los datos del usuario

- /root: Carpeta principal del sistema

## Comandos

- `df (disk file system)` : Da informacion detallada del espacio usado en los discos
  
  - -Th : Tipo de sistemas de archivos legible para humanos

- `lsblk (List block device)`: Informacion sobre el bloque de dispositivos
  
  - -f: Mas detalle

- `fsck (File system check)`: Verifica y repara el sistema de archivos

- `blkid`: Informacion sobre bloques de dispositivos disponibles "root"

- `cfdisk`: Permite ver las particiones de discos y gestionarlas

- `fdisk`: Permite ver los discos del sistema
  
  - -l: "Mas detalle"
