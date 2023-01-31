## Docker
- Automatizacion de despliegue de aplicaciones en contenedores
- Contenedor: Compuesto de codigo, librerias, dependecias para que funcione un proceso
- Multiplataforma
|Contenedor|Maquina Virtual|
|---|---|
|Manejador por el docker engine y con las librerias necesarios|Manejado por el hipervisor y sistema operativo embebido con las librerias del mismo|
- Integra CD/CI

## Conceptos Basicos
- Cliente administra al daemon el cual tiene los contenedores o imagenes las cuales son obtenidas del registro de docker hub
- Contenedores creados a partir de imagenes
- Imagenes: Sistema der archivos y configuracion para crear contenedores
- Containers: Ejecucion la instancia de docker, con todas las dependencias
- Docker hub: Repositorio publico en nube de imagenes
- `docker run -d nginx` "background"
- `docker rm`
- `docker rmi`
- `docker run ... [comando]`
- `docker exec [comando]`
- `docker logs`
- `docker kill`

## Redes en Docker
- Puertos privados por lo que para que sean publicos se deben mapear con el puerto del host
- `docker network`
- `docker inspect container > container.txt`
- `docker network inspect red > red.txt`
- `docker network create`
- `docker network create --subnet=192.168.0.0/16 red2`
- `docker run ... --network red2 ...`
- `docker network connect red container`
- Detener contenedores antes de borrar

## Docker Volumenes y Puertos
Mecanismo para conservar datos generador por contenedores
Tipos de volumenes y montajes:
- Anonumous volumes
- Named volumes
- Bind mounts: Conexion de alto rendimiento del contenedor a maquina host
	- Comparte archivo ya sea de lectura o escritura
	- `docker run ... -v $(pwd):/home ...`
- Volume Create:  Ruta por defecto para volume host es cual puede ser anclado para persistencia de datos y comunicacion entre contenedores
	- `docker volume create data`
	- `docker volume inspect data`
	- `docker run --moun source=[name], destrinatios[path cont]`
	- `docker run ... --mount ..., readonly`
	- Eliminar contenedores antes de borrar volumenes
	- `docker volume rm` || `docker volume prune`

## Puertos
Puerto privador para prublicarlos `--public` o `-p` creara regla de firewall que contecta puerto de contenedor a host