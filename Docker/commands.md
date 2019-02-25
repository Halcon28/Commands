# Comandos para docker

## Basicos

Buscar una imagen en docker hub
```
docker search "name"
```

Descargar una imagen desde docker hub
```
docker pull "name"
```

Listar las imagenes que ya estan instaladas
```
docker images
```

Ejecutar una imagen en docker
```
docker run "name"
```

Listar las imagenes en ejecucion
```
docker ps
```

Listar las imagenes en ejecucion o ejecutadas
```
docker ps -a
```

Vuelve a iniciar una imagen terminada
```
docker start ########
```

Entrear a una imagen en ejecucion
```
docker attach ########
```

Detener una imagene en ejecucion
```
docker stop ########
```

## Administrar imagenes
Eliminar Imagen
f => forzar
```
docker rmi -f #########
```

## Comandos sobre las imagenes

Ver los directorios de la imagen
```
docker run "name" ls
```

Asignar un nombre personalizado a una imagen mientras se esta ejecutando
```
docker run --name "nombre" "imagen"
```

Crear una nueva imagen
```
docker commit ######## "name"
```

Crear una imagen a partir de un archivo
```
docker build -t "name" /home/user/path
```

## comandos docker-ubuntu

Correr un bash
i => interactive
t => pseudo-TTY
```
docker run -i -t ubuntu bash
```

### Apache
Crear una imagen con apache
```
docker commit --change='CMD ["apache2ctl", "-D FOREGROUND"]' -c "EXPOSE 80" ######## "name"
```

Correr una umagen con apache
p => puerto
```
docker run -d -p "puerto-localhost"80:80 "name"
```

## Dockerfiles
Estructura

> **FROM** ubuntu:16.04

> **MAINTAINER** user mail

> **RUN** apt-get update

> **RUN** apt-get -y install apache2

> **EXPOSE** 81

> **CMD** /usr/sbin/apache2ctl -D FOREGROUND
