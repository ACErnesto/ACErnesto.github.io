# Acordeon

### Touch  poner el 

### $ git init 
- Inicializa un proyecto
### configurar las variables de git
**git config --global user.name "Ernesto Alcantara"**
**git config --global user.email "lu_fra_ernes@hotmail.com"**
**git config --global core.editor "nano"**


### $  git status
- Muestra el estado actual de los archivos del proyecto
- Comando
**git status**
### $  git add
- Este comando empieza a seguir uno o mas archivos y los agrega al área de preparación, genrando un nuevo estado del proyecto
- La bandera -A agrega todos los archivos del repositorio. 
- Comando
**git add ACORDEON.md**  #Donde el "ACORDEON.md" es el nombre del archivo
### $  git commit
- Registra nuevo estado y lo registra en la historia de nuestro reposiorio.
- Por lo general este comando se usa con la bandera -m y un pequeño texto que describa lo que se hizo.
- Comando
**git commit -m "primer commit"**

### $  git log
Comando que muestra el histrial de commints que hamos hecho en nuestro proyecto.
- La bandera --online muestra cada entrada en una sola lnea
- Es posible tver el histirial de un solo archivo, pasando como argumento el nombre del éste
- Comando 
**git log**
**git log --oneline**




