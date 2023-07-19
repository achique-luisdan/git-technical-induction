##  1. CLONAR REPOSITORIO

```
git clone URL
```

## 2. NAVEGAR RAMAS 

### Listar ramas
```
git branch
```

### Crear ramas
```
git branch RAMA
```

### Mover a rama
```
git checkout RAMA
```

## 3. BAJAR CAMBIOS

### Baja (y fusión local)
```
git pull
```

### Baja
```
git fetch remote RAMA
```

## 4. SUBIR CAMBIOS 

### Consulta cambios
```
git status
```

### Añade cambios (todos)
```
git add .
```

### Comenta cambios
```
git commit -m "COMENTARIO"
```

### Sube cambios (al servidor)

```
git push origin RAMA
```

## 5. FUSIONAR RAMAS

### Cambiar a rama
```
git checkout RAMA-BASE
```

### Fusiona rama
```
git merge RAMA-FUSIONAR
```

### Sube fusión (al servidor)
```
git push origin RAMA-BASE
```

### Abortar fusión
```
git merge --abort
```


## Fusionar archivos o carpetas específicas
```
git checkout source_branch -- path/to/file
```

## 6. PODAR RAMAS

### Elimina rama local de tu computadora
```
git branch -d RAMA
```

### Elimina rama remota del servidor
```
git push origin --delete RAMA
```

## 7. CONFIGURAR FLUJO

master

qa

feat-

bug-

release-

fix-

v

* Mejora * Error en dev o qa * Entregable * Error en master o producción * Etiqueta de versión

## 8. INICIAR MEJORA O ERROR

### Crea mejora
```
git flow feature start MEJORA
```

### Publica mejora en el servidor
```
git flow feature publish MEJORA
```

### Crea error desde qa
```
git flow bugfix start ERROR
```

### Publica error desde qa en el servidor
```
git flow bugfix publish ERROR
```

### Crea error desde master o producción
```
git flow hotfix start ERROR
```

### Publica error desde master o producción en el  servidor
```
git flow hotfix publish ERROR
```

## 9. FINALIZAR MEJORA O ERROR

### Finaliza mejora

```
git flow feature finish MEJORA
```

### Finaliza error desde qa
```
git flow bugfix finish ERROR
```

### Finaliza error desde master o producción
```
git flow hotfix finish ERROR
```
