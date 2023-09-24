# MongoDB

### Contenedor

```
docker run -d --name server-mongo -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=12345 -e MONGO_INITDB_DATABASE=course mongo:3.6.23
```

### Cliente

```
docker run -d --name client-mongo -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=12345 -e ME_CONFIG_MONGODB_SERVER=172.17.0.5 --publish published=9100,target=8081 mongo-express
```
