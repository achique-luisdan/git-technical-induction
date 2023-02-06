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

## 6. PODAR RAMAS

### Elimina rama local de tu computadora
```
git branch -d RAMA
```

### Elimina rama remota del servidor
```
git push origin --delete RAMA
```
