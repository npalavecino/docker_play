# Repositorio de estudio docker
Comando Basicos Docker 


```sh 
docker run hello-world
Corre el contenedor más básico de docker.
```

```sh 
$ docker ps 
Ver los contenedores que estamos corriendo en el momento.
```

```sh 
$ docker ps -a 
Ver todos los contenedores que se han corrido en la máquina.
```

```sh 
$ docker run --name <name> <image> 
colocar un nombre custom al contenedor
```

```sh 
$ docker rename <actual-name>
```

```sh 
 Inspecionar la config un contenedor
$ docker inspect <container_id or container_name>
```

```sh 
$ docker exec  <container_id or container_name> bash  
Ingresar a consola en modo interactivo y ejecutar un comando bash 
```

```sh 
docker rm -f $(docker ps -aq)
Eliminar todos los contenedores
```



```sh 
$ docker images ls 
Lista todas las imagenes 
```


```sh 
docker pull <image_name>:<tag_version>
Descargar desde dockerhub 
```



