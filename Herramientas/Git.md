# Descripción 

Es un software de control de versiones, que nos permite gestionar y publicar nuestros 
proyectos, así como la creación de puntos de control durante el desarrollo de los mismos.

## Comandos que más uso

### Crear o establecer una identidad de persona a nivel local

```Git
git config user.name "nombre de usuario"
git config user.email "email"
```

## Inicio del repositorio

```Git
git init
```

### Clonar proyectos existentes

```Git
git clone "url" "ruta"
```

### Creación y renombrado de una rama

```Git
git branch -m
```

### Creación una rama a partir de la rama actual

```Git
git checkout -b "nombreRama"
```

## Cambio entre ramas existentes

```Git
git checkout "nombreRama"
```

### Comprueba el estado del repositorio

```Git
git status
```

### Tipos de estado

untraked = Nuevos archivos
staged = Preparado para el commit

### Añadir archivos

```Git
git add "archivo" o no
```

## Crear un commit

```Git
git commit
git commit -m "Título"
git commit -m "Título" -m "SubTítulo"
```

### Mostrar los commits

```Git
git log
git log -n "numero de commits"
```

### Ver repositorios remotos

```Git
git remote
```

## Añadir repositorios remotos

```Git
git remote add "name" "identity"
```

### Subir los cambios a la rama remota

```Git
git push
git push "remoto" "rama"
```

### Vincula el push al remoto

```Git
git push -u "remoto" "rama"
```

### Traerse los cambios de la misma rama

no notifica los conflictos

```Git
git pull
```

### Traerse los cambios de otra rama

notifica los conflictos

```Git
git merge
```

### Eliminar commits del log

```Git
git rebase -i "hash del commit padre"
```

### Abortar Rebase

```Git
git rebase --abort
```

### Estructura de ramas recomendada

```Git
# Ramas
## main
## dev
```

### Generar clave ssh

Para comunicarse con el servidor de Github, de una manera mas segura
es aconsejable utilizar una conexión cifrada, mediante el par de claves
publica - privada.

Para ello generamos el par de claves con el siguiente comando:

Windows:
> ssh-keygen -b 4096 -C "email" -t rsa

Después en Github, en el sub-apartado SSH y GPG Keys de Opciones, introducimos la clave pública.

Para indicarle a Git que vamos a añadir una fuente remota mediante este método
simplemente copiamos el enlace que aparece en el apartado "code" del repositorio.

Ejemplo:
> git@github.com:altaskur/Buscaminas.git

git remote add "name" "identity"
> git remote add "origin" "git@github.com:altaskur/Buscaminas.git"
