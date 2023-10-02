# Drupal

### Servidor

```
docker run -d --name server-postgres -e POSTGRES_DB=db_drupal -e POSTGRES_PASSWORD=12345 -e POSTGRES_USER=user_drupal postgres
```

_No es necesario exponer el puerto si nos conectamos desde la misma red de docker_

```
docker run -d --name server-postgres -e POSTGRES_PASSWORD=12345 postgres:11.21-alpine3.17
```

### Cliente

```
docker run -d --name client-postgres --publish published=9500,target=80 -e PGADMIN_DEFAULT_PASSWORD=54321 -e PGADMIN_DEFAULT_EMAIL=sergiohidalgocaceres@gmail.com dpage/pgadmin4
```

_agregar la extensión pg_trgm_

### Drupal

```
docker run -d --name server-drupal --publish published=9600,target=80 drupal
```

### Agregar contenedores a una red

```
docker network create net-postgres -d bridge
docker network connect net-postgres server-postgres
docker network connect net-postgres client-postgres
docker network connect net-postgres server-drupal
```
