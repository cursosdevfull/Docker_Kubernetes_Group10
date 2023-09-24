# Jenkins

### Crear un contenedor

```
docker run -d --name server-jenkins -p 8080:8080 -p 50000:50000 jenkins/jenkins:alpine3.18-jdk11
```

### Para acceder al contenedor

```
docker exec -it server-jenkins sh
```
