# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
# COMPLETAR
docker pull hello-world

**¿Qué es nginx**
# COMPLETAR 
NGINX es una herramienta multifunción. Con NGINX, puede utilizar la misma herramienta que su balanceador de carga, proxy inverso, caché de contenido y servidor web, lo que minimiza la cantidad de herramientas y configuraciones que su organización necesita mantener.

Descargar la imagen  **nginx** en la versión **alpine**
# COMPLETAR
docker pull nginx:alpine

### Listar imágenes

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 
<img width="811" height="136" alt="image" src="https://github.com/user-attachments/assets/3474f7f4-266f-4703-8af6-6f7e1267c0ce" />

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
# COMPLETAR
<img width="1450" height="1268" alt="image" src="https://github.com/user-attachments/assets/c9f570b9-b40e-4157-a6a1-9f4a554d16d0" />

<img width="1313" height="1281" alt="image" src="https://github.com/user-attachments/assets/6da8bbda-c64a-47fe-8c2f-74d29269ec47" />



**¿Con qué algoritmo se está generando el ID de la imagen**
Se está generando con el algoritmo sha256

# COMPLETAR

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
# COMPLETAR
docker rmi hello-world:latest
<img width="1007" height="104" alt="image" src="https://github.com/user-attachments/assets/44675ede-d39a-4d7b-9052-c2b0d16574a7" />
<img width="912" height="105" alt="image" src="https://github.com/user-attachments/assets/145af51c-aa07-4b01-ba1d-d65cb847a83d" />


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
