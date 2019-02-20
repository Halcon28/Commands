# Comandos de GitHub

## Coamndos basicos
Agregar un repositorio remoto al proyecto actual
```
git remote add origin https://github.com/usuario/proyecto.git
```

Ver el origen remoto del proyecto
```
git remote -v
```

Agregar un commit al repositorio remoto (-u pone el origen por default)
```
$ git push -u origin master
```

Actualiza el proyecto local con los cambios del origen remoto
```
git pull
```

## Hacer push de los tags

git push --tags

## Clonar repositorio
```
git clone https://github.com/usuario/proyecto.git nuevo-nombre
```

## Merge de un commit local con uno remoto
```
git fetch
git pull
git push
```

## Definir un nuevo repositorio remoto
```
git remote add upstream https://github.com/usuario/proyecto
```