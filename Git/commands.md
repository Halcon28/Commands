## Comandos de git

Muestra las diferencias entre el ultimo commit y los cambios actuales
```
git diff
```

Muestra las diferencias entre el ultimo commit y los cambios actuales en el stage
```
git diff --staged
```

Elimina un archivo del stage
```
git reset HEAD "Archivo.ext"
```

Regresa los cambio al ultimo commit
```
git checkout -- "Archivo.ext"
```

Muestra todos los commit que han existido aunque ya no esten en el log
```
git reflog
```

Realiza el stage y commit al mismo tiempo
```
git commit -am "mensaje"
```

Actualiza el mensaje del ultimo commit
```
git commit --amend -m "mensaje nuevo"
```

Resetea el ultimo commit manteniendo los cambios actuales(despues se debe de hacer el commit normal)
```
git reset --soft HEAD^
```

Resete el proyecto al commit deseado perdiento los cambios mas recientes
```
git reset --hard bfa8d59
```

Cambia el nombre a un archivo manteniendo el registro de git
```
git mv "archivo.ext"
```

Elimina un archivo del repositorio
```
git rm "archivo.ext"
```

Renombrar un archivo sin git
```
Primero se renombra sin git y despues se corren los comandos
git add -u
git add -A
```

Eliminar un archivo sin git
```
Primero se elimina sin git y despues se corren los comandos
git add -u
```

Crear una nueva rama
```
git branch "nueva-rama"
```

Cambiar de rama
```
git checkout "nueva-rama"
```

Crea y se mueve a la rama creada
```
git checkout -b rama-villanos
```

Ver las ramas del proyecto y saber en cual se encuentra
```
git branch
```

Une una rama con la rama actual
```
git merge "nueva-rama"
```

Eliminar una rama(Buena practica eliminarla cuando ya se hizo el merge)
```
git branch -d "nueva-rama"
```

Crear un Tag de un commit
```
git tag "tagName"
```

Crear un tag con anotacion
```
git tag -a v1.0.0 345d7de -m "Descripcion"
```

Ver los tag existentes
```
git tag
```

Ver los datalles del commit en base al tag
```
git show v1.0.0
```

Eliminar un tag
```
git tag -d "tagName"
```

Git Stash - Mueve todos los cambios despues del ultimo commit a un contenedor temporarl
```
git stash ó git stash save
```

Git Stash con mensaje para identificarlo
```
git stash save "Mensaje del stash"
```

Ver los stash pendeintes
```
git stash list
```

Ver los stash pendeintes de forma mas detallada
```
git show stash
```

Restaura un stash determinado, si no se especifica uno se tomara el mas reciente
```
git stash apply ó git stash apply stash@{1}
```

Restaura el stash y lo elimina al mismo tiempo
```
(git stash apply y git stash drop) ó git stash pop
```

Elimina el ultimo stash creado
```
git stash drop
```

Limpia todos los stash que existan
```
git stash clear
```