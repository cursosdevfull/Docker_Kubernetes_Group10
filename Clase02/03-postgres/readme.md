# Postgres

### Servidor

```
docker run -d --name server-postgres --publish published=5432,target=5432 -e POSTGRES_PASSWORD=12345 postgres:11.21-alpine3.17
```

_No es necesario exponer el puerto si nos conectamos desde la misma red de docker_

```
docker run -d --name server-postgres -e POSTGRES_PASSWORD=12345 postgres:11.21-alpine3.17
```

### Cliente

```
docker run -d --name client-postgres --publish published=9500,target=80 -e PGADMIN_DEFAULT_PASSWORD=54321 -e PGADMIN_DEFAULT_EMAIL=sergiohidalgocaceres@gmail.com dpage/pgadmin4
```

### Agregar contenedores a una red

```
docker network create net-postgres -d bridge
docker network connect net-postgres server-postgres
docker network connect net-postgres client-postgres
```
