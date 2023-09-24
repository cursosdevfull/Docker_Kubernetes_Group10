# Redis

### Crear un contenedor de Redis

```
docker run -d --name server-redis -p 6379:6379 redis:alpine
```

### Usando una forma más semántica cuando se especifican puertos

```
docker run -d --name server-redis2 --publish published=6380,target=6379 redis:alpine
```

### Publicando todos los puertos

```
docker run -d --name server-redis3 --publish-all redis:alpine
```
