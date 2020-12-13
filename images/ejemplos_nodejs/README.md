1.- Construir  imagen basada en Dockerfile

```sh 
$ docker build -t <tag_nombre> 
```  

2.- Comando para listar imagen creada con su tag 
```sh 
$ docker images ls
```  

3.- Crear contenedor  con la instrucción de borrarse una vez sea detenido. 
Exponer el puerto 3000 del contenedor el puerto 3000 del host(maquina anfitriona)
```sh 
$ docker run --rm -p 3000:3000 <tag_images> 
```  


#####################################################

Explicación de archivo Dockerfile

```sh 

# especifica la imágen base, para este caso se trata de node con especificación de versión 12
FROM node:12

# copiar todo lo que existe en el directorio actual (durante el build, es decir se refiere al directorio de nuestra máquina host/anfitrión), 
# en el directorio /usr/src/ del contenedor, es así como al final podemos ejecutar el archivo index.js, dado que se encuentra en el 
# conjunto de archivos que copiamos desde nuestra máquina al contenedor.
COPY [".", "/usr/src/"]

# establecer el directorio de trabajo, similar a utilizar el comando cd /usr/src
WORKDIR /usr/src

# descargar las dependencias del proyecto al ejecutar el comando de npm (node package manager)
RUN npm install

# Expone este puerto del contenedor, es decir, lo pone a la escucha
EXPOSE 3000

# ejecuta el comando node index.js en el contenedor ya creado
CMD ["node", "index.js"]

``` 
