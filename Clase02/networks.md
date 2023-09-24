# Operaciones con Redes

### Crear una red de tipo bridge

```
docker network create net-course -d bridge
```

### Crear un contenedor vinculado a una red

```
docker run -d --name server01 --network net-course nginx:alpine
docker run -d --name server02 --network net-course nginx:alpine
docker run -d --name server03 --network net-course nginx:alpine
docker run -d --name server04 nginx:alpine
```

### Para saber a qué red está conectado un contenedor

```
docker inspect server01
docker network inspect net-course
```

### Vincular contenedor a una red

```
docker network connect net-course server04
```

### Para desvincular un contenedor a una red

```
docker network disconnect net-course server04
```
