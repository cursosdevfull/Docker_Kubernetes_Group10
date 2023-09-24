# MySQL

### Para crear un contenedor con MySQL

```
docker run -d --name <nombre contenedor> -e MYSQL_ROOT_PASSWORD=<valor> mysql:8
```

### Para crear un contenedor con MySQL creando un usuario no-admin

```
docker run -d --name <nombre contenedor> -e MYSQL_ROOT_PASSWORD=<valor> -e MYSQL_DATABASE=<nombre base de datos> -e MYSQL_USER=<nombre del usuario> -e MYSQL_PASSWORD=<contraseña del usuario> mysql:8
```

### Para crear un contenedor de MySQL usando variables de entorno desde un archivo plano

```
docker run -d --name <nombre contenedor> --env-file=variables.txt mysql:8
```

### Cliente de MySQL (PhpMyAdmin)

```
docker run -d --name phpmyadmin --publish published=8010,target=80 -e PMA_ARBITRARY=1 phpmyadmin
```
