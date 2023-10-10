# Instalar librerías desde un contenedor

```
docker run --rm -v $(pwd -W)/lib:/app/node_modules <nombre de imagen> install bootstrap
```
