# Apache

### Crear volumen

```
docker volume create vol-apache
```

### Servidor apache

```
docker run -d --name server-apache -v vol-apache:/usr/local/apache2/htdocs/ --publish published=9200,target=80 httpd:2.4
```
