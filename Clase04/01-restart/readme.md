# Restart

### restart = no

No reinicia el contenedor bajo ninguna razón

### restart = always

Si se detiene manualmente, no se reinicia. El contenedor es iniciado nuevamente cuando el demonio (servicio) reinicia

```
docker run -d --name <nombre contenedor> --restart always <nombre imagen>
```

### restart = unless-stopped

Se reinicia siempre y cuando no se detenga manualmente

```
docker run -d --name <nombre contenedor> --restart unless-stopped <nombre imagen>
```

### restart = on-failure

Se reinicia únicamente cuando hay una falla en la ejecución del código. No se reinicia si el contenedor se detiene manualmente.

```
docker run -d --name <nombre contenedor> --restart on-failure <nombre imagen>
```
