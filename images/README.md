


Comandos basicos para construcción de imagenes 


```sh 
$ docker build -t ubuntu:platzi .
Creo una imagen con el contexto de build <directorio>)
```

```sh 
$ docker run -it ubuntu:platzi
corro el contenedor con la nueva imagen
```

```sh 
$ docker login
logueo en docker hub
```

```sh 
$ docker tag ubuntu:platzi <miusuario>/ubuntu:exaple 
cambio el tag para poder subirla a mi docker hub
```

```sh 
$ docker push miusuario/ubuntu:example
publico la imagen a mi docker hub
```

