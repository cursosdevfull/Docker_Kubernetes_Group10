# Operaciones con contenedores

### Para ingresar a un contenedor

```
docker exec -it <nombre o id del contenedor> <comando del programa o librería a ejecutar>
```

### Para ver los logs de un contenedor

```
docker logs <nombre o id del contenedor> < -n cantidad de líneas> -t (para incluir la fecha y la hora)
```

### Para crear un contenedor con variables de entorno

```
docker run -d --name server-nginx -e username=sergio -e role=admin nginx:alpine
```
