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


## Branch
- Una rama (branch) es, en pocas palabras,  una línea independiente de trabajo, la cual no afecta a nuestra rama principal (master), sin embargo, tiene la capacidad de fusionarse con otras ramas, incluida la principal.
- -lista de ramas existentes en el repositorio.
-- si se le agrega [<nombre>] de rama como argumento, se creará una rama con ese nombre

- #### Actividad
- crear una nueva rama proyecto
- Hacer un checkout a la rama
- Crear un archivo index.html y estilos.css
- Hacer commit


- Comandos
-- `git branch proyecto`
-- `git checkout` proyecto cambio al proyecto o rama
-- `git branch` enlista y marca la rama en la que actualmente se trabaja.


## git merge
-Este comando fusiona dos  ramas, fusiona una rama objetivo con la rama donde nos encontramos actualmente
-- Recibe como párametro la rama objetivo

- Actividades
-- Crear una nueva rama llamada inicio
-- Hacer checkout
-- Modificar el index.html con las siguientes instrucones 
-- Hacer commit 
-- y regresar a la rama proyecto y hacer un merge

- Comando
-- `git checkout -b inicio`, forma simplificada para crear una nueva rama y cambiarse a esta.
-- `git branch inicio`
-- `git checkout inicio`
-- `git diff` es para saber que cambios se realizaron en el codigo antes de hacer commit. Pone en rojo los cambios anteriores.
`git add -A`
`git status`
`git commit -m "Sección de inicio modificada"`
`git checkout proyecto`
`git merge inicio`, se trae los cambios a la rama "proyecto"


## Conflictos de merging

- A veces si se está trabajando en 2 ramas al mismo tiempo, modificando un mismo archivo, se pueden generar conflictos, por lo que es necesario corregirlos.


Actividades
- Crear una rama "seccion1
- Sobre la rama 'proyecto' agregar un encabezado a la seccion1
- Hacer commit de los cambios
- Cambarse a la rama "seccion1"
- Agregar un encabezado adecuado a seccion1 y hacer commit de los cambios
- Regresar a proyecto

-Commando
-- `git status seccion`
-- `git checkout proyecto`
-- `nano index.html`, hago una modificación en seccion uno
-- `git add -A`
-- `git commit -m "Sección de uno modificada"`
-- `git checkout seccion1`
-- `nano index.html`, hago una modificación en seccion uno
-- `git add -A`
-- `git commit -m "Modificacion en seccion1"`, la misma que la anterior
-- `git checkout proyecto`
-- `git merge seccion1`, aqui surge el conflicto.

#### Corregir el error
-- `nano index.html`, modificar de nuevo el archivo
-- `git add -A`
-- `git status`
-- `git commit -m "Correccion de merging"`


Sourcetreeapp mac y windows
gitkraken linux, mac y windows






