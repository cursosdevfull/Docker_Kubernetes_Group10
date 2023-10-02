# Volúmenes

## HOST

### Volúmen tipo host

```
docker run -d --name server-nginx --publish published=5000,target=80 -v D:\\Cursos\\Docker_Kubernetes_Group10\\Clase02\\05-nginx\\html:/usr/share/nginx/html nginx:alpine
```

### Volumen tipo host usando PWD (Git Bash)

```
docker run -d --name server-nginx --publish published=5000,target=80 -v $(pwd -W)/html:/usr/share/nginx/html nginx:alpine
```

### Volumen tipo host usando PWD (en Linux)

```
docker run -d --name server-nginx --publish published=5000,target=80 -v $(pwd)/html:/usr/share/nginx/html nginx:alpine
```

### Volumen tipo host usando PWD y PowerShell

```
docker run -d --name server-nginx --publish published=5000,target=80 -v $(pwd)/html:/usr/share/nginx/html nginx:alpine
```

## NOMBRADO

### Crear volumen

```
docker volume create vol-postgres
docker volume create vol-drupal-sites
docker volume create vol-drupal-themes
docker volume create vol-drupal-profiles
docker volume create vol-drupal-modules
```

### Crear una red para drupal

```
docker network create net-postgres -d bridge
```

### Servidor postgres

```
docker run -d --name server-postgres -e POSTGRES_DB=db_drupal -e POSTGRES_PASSWORD=12345 -e POSTGRES_USER=user_drupal -v vol-postgres:/var/lib/postgresql/data --network net-postgres postgres
```

### Cliente postgres

```
docker run -d --name client-postgres --publish published=9500,target=80 -e PGADMIN_DEFAULT_PASSWORD=54321 -e PGADMIN_DEFAULT_EMAIL=sergiohidalgocaceres@gmail.com --network net-postgres dpage/pgadmin4
```

_agregar la extensión pg_trgm_

### Drupal

```
docker run -d --name server-drupal --publish published=9600,target=80 -v vol-drupal-modules:/var/www/html/modules -v vol-drupal-profiles:/var/www/html/profiles -v vol-drupal-sites:/var/www/html/sites -v vol-drupal-themes:/var/www/html/themes --network net-postgres drupal
```

## ANÓNIMO

```
docker run -d --name server-nginx -v /usr/share/nginx/html --publish published=9800,target=80 nginx:alpine
```

### Para eliminar el contenedor y el volumen

```
docker rm -fv server-nginx
```

_esta instrucción elimina el volumen si éste es de tipo anónimo_
