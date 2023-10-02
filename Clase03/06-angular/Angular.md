# Angular

### Crear contenedor

```
docker run -d --name server-angular --publish published=9100,target=80  -v $(pwd -W)/dist/06-angular:/usr/share/nginx/web:ro -v $(pwd -W)/conf/default.conf:/etc/nginx/conf.d/default.conf:ro nginx:alpine
```
