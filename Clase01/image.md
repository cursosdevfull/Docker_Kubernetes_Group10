# Comandos para imágenes

### Listar imágenes

```
docker images
```

### Filtrar imágenes

```
docker images | grep <termino a buscar>
```

### Inspeccionar una imagen

```
docker image inspect <nombre de la imagen>
docker image inspect <nombre de la imagen>:<tag>
```

### Descargar imagen

```
docker pull <nombre imagen>
docker pull <nombre imagen>:<tag>
```

### Para eliminar una imagen

```
docker rmi <nombre imagen>:<tag>
docker rmi -f <nombre imagen>:<tag>
```
