# Limitar uso de memoria y procesador

### Memoria

```
docker run -d --name server-nginx --memory=10m nginx:alpine
docker run -d --name server-nginx --memory=300m --memory-swap=1g nginx:alpine
```

### Procesador

```
docker run -d --name server-nginx --cpus="1.5" nginx:alpine
docker run -d --name server-nginx --cpuset-cpus="0-2" nginx:alpine
docker run -d --name server-nginx --cpuset-cpus="1,3" nginx:alpine
```
