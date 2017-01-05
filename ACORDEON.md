# Acordeon

### Touch  poner el 

### $ git init 
- Inicializa un proyecto
### configurar las variables de git
-- `git config --global user.name "Ernesto Alcantara"`
-- `git config --global user.email "lu_fra_ernes@hotmail.com"`
-- `git config --global core.editor "nano"`


### $  git status
- Muestra el estado actual de los archivos del proyecto
- Comando
-- `git status`
### $  git add
- Este comando empieza a seguir uno o mas archivos y los agrega al área de preparación, genrando un nuevo estado del proyecto
- La bandera -A agrega todos los archivos del repositorio. 
- Comando
- Agregar cada archivo
-- `git add ACORDEON.md` 
-- `git add -A`
>Donde el "ACORDEON.md" es el nombre del archivo. La bandera -A agrega todos los archivos.
### $  git commit
- Registra nuevo estado y lo registra en la historia de nuestro reposiorio.
-- Por lo general este comando se usa con la bandera -m y un pequeño texto que describa lo que se hizo.
- Comando
-- `git commit -m "primer commit"`

### $  git log
- Comando que muestra el histrial de commints que hemos hecho en nuestro proyecto.
-- La bandera --online muestra cada entrada en una sola linea, historial completo de commits del repo, o de un archivo si se especifica
-- Es posible tver el histirial de un solo archivo, pasando como argumento el nombre del éste
-- Comando 
-- `git log`
-- `git log --oneline`

## .gitignore
- Archivo que permite ignorar archivos o directorios, los cuales no queremos que entren en el seguimiento de nuestro repositori

> Nombre de archivo y salto de linea
- Nombres de los archivos o carpetas
- wildcards *

-- Comando
- `nano .gitignore`
Agregar el nombre o nombres de los archvios

> El archivo permanece oculto .gitignore
## $ git checkout
- Comando que permite movernos entre commits o incluso ramas de nuestro repositorio.
-- Lleva como argumento el id del commit o parte de.

- Comando
-- `git log`  listar todos los commits
-- `git checkout 1ee0ec3` ir a alguna rama o estado 
-- `git checkout master` regresar a la rama o estado principal

> Al saltar a un estado es mejor hacer una nueva rama

##  $ git revert
-Este comando nos revierte un cambo ya registrado, creando un nevo commit.
-- Lleva como argumento el id del commit a revertir

- Comando
--  `rm ACORDEON.md`
-- `git add -A`
-- `git commit -m "nuevos cambios"`
-- `git log --oneline`
-- `git revert 14bf088078`
-- `git status & git log`

> En cada paso pondremos `git add -A` y `git commit -m "nuevos cambios"' 


## $ git reset
- Regresa al último estado guardado, borrado permanentemente cualquier cambio en el área de pruebas
-- Leva la bandera --hard

> Este comando trabaja sobre los cambios antes de hacer commit.

## $ git clean

-Borra permanentemente los archivos no seguidos
-- LLeva la bandera -f

- Comando
- `git log --oneline`
- `nano ACORDEON.md` aquí alguna modificación
- `nano prueba.md` un nuevo archivo
- `git add ACORDEON.md` agregar a git
- `git status` verificar el status
- `git reset --hard`
- `git clean -f`







