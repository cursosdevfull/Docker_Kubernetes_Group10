# Volúmenes

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
