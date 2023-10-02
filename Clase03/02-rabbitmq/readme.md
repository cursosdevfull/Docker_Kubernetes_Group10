# Rabbitmq

### Crear contenedor

```
docker run -d --name server-rabbitmq --publish published=15672,target=15672 --publish published=5672,target=5672 rabbitmq:3.9.22-management-alpine
```
