# GIT
## INFORMACIÓN
### Definición
Git es un **sistema de control de versiones distribuido de código abierto** desarrollado por Linus Torvalds, el creador de Linux.

El control de versiones distribuido *permite a los desarrolladores descargar un software, realizar cambios y subir la versión que han modificado.* Todas las modificaciones subidas se guardan en versiones independientes, _no sobrescribiendo en el archivo original._

La diferencia entre el control de versiones y Git, es que en Git cada desarrollador tendrá en el ordenador una copia del código fuente original y de las versiones disponibles del proyecto, permitiendo la ramificación y fusión.

### ¿Qué es GITHub y para qué sirve?
Github es un repositorio online gratuito que __permite gestionar proyectos y controlar versiones de código.__ Es muy utilizado por desarrolladores para almacenar sus trabajos dando así la oportunidad a millones de personas de todo el mundo a cooperar en ellos.

Se podría hablar de Github como la red social pensada para desarrolladores, siendo este repositorio uno de los más usados a nivel mundial.

Podemos seguir e interactuar con personas interesadas en un tipo de proyecto en concreto, dando a conocer los nuestros o cooperando en el proyecto de terceros.


### Partes de Github
#### Repositorio
Un repositorio es la **ubicación o ruta en la que se almacena toda la información** de un proyecto como imágenes, código, carpetas, documentos, etc.

Cada proyecto contaría con su propio repositorio único, por lo que la ruta de acceso será exclusiva para el proyecto.

#### Branch (ramificaciones)
En el caso de que queramos trabajar una parte concreta de nuestro proyecto de forma aislada no afectando al repositorio principal, tendremos que hacerlo mediante Branch.

__El Branch creará una copia exacta de nuestro proyecto para hacer pruebas__ sin miedo a equivocarnos y que afecte a todo el trabajo realizado.
#### Pull Request (Fusión)
Cada vez que subas un nuevo cambio en una rama del proyecto, puedes avisar a los demás colaboradores para que validen o no tu pull request, o si encuentran posibles mejoras poder comentarlas.

#### Tag
Los Tag **permiten controlar el estado de un repositorio dando información** a otros usuarios de en qué versión se encuentra actualmente el proyecto.

Esta acción es conocida como “Tagging” y es bastante importante a la hora de gestionar la vida de un proyecto.
Crear un nuevo proyecto a partir de otro (Fork).

#### Fork
Una opción bastante usada en Github es la de Fork. Con esta opción podrás crear un nuevo proyecto en base a uno ya creado, permitiendo hacer modificaciones y guardándose en tu propio repositorio y no en el repositorio original.

Esta opción facilita el crecimiento de proyectos __permitiendo a los desarrolladores continuar mejorando un software por cuenta propia__ y en el caso de realizarse una mejora en el repositorio principal podrás __también implementarla a tu proyecto clonado.__

Esta opción es conocida en Github como bifurcación.
## GUÍA DE COMANDOS
### Configuración Básica

Configurar Nombre que salen en los commits
```ssh
	git config --global user.name "dasdo"
```
Configurar Email
```ssh	
	git config --global user.email dasdo1@gmail.com
```
Marco de colores para los comando
```ssh
	git config --global color.ui true
```

### Iniciando repositorio

Iniciamos GIT en la carpeta donde esta el proyecto
```ssh
	git init
```
Clonamos el repositorio de github o bitbucket
```ssh
	git clone <url>
```
Añadimos todos los archivos para el commit
```ssh
	git add .
```
Hacemos el primer commit
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
```
subimos al repositorio
```ssh
	git push origin master
```

### GIT CLONE


Clonamos el repositorio de github o bitbucket
```ssh
	git clone <url>
```
Clonamos el repositorio de github o bitbucket ?????
```ssh
	git clone <url> git-demo
```

### GIT ADD


Añadimos todos los archivos para el commit
```ssh
	git add .
```
Añadimos el archivo para el commit
```ssh
	git add <archivo>
```
Añadimos todos los archivos para el commit omitiendo los nuevos
```ssh
	git add --all 
```
Añadimos todos los archivos con la extensión especificada
```ssh
	git add *.txt
```
Añadimos todos los archivos dentro de un directorio y de una extensión especifica
```ssh
	git add docs/*.txt
```
Añadimos todos los archivos dentro de un directorios
```ssh
	git add docs/
```
### GIT COMMIT

Cargar en el HEAD los cambios realizados
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
```
Agregar y Cargar en el HEAD los cambios realizados
```ssh
	git commit -a -m "Texto que identifique por que se hizo el commit"
```
De haber conflictos los muestra
```ssh
	git commit -a 
```
Agregar al ultimo commit, este no se muestra como un nuevo commit en los logs. Se puede especificar un nuevo mensaje
```ssh
	git commit --amend -m "Texto que identifique por que se hizo el commit"
```
### GIT PUSH

Subimos al repositorio
```ssh
	git push <origien> <branch>
```
Subimos un tag
```ssh
	git push --tags
```
### GIT LOG

Muestra los logs de los commits
```ssh
	git log
```
Muestras los cambios en los commits
```ssh
	git log --oneline --stat
```
Muestra graficos de los commits
```ssh
	git log --oneline --graph
```
### GIT DIFF

Muestra los cambios realizados a un archivo
```ssh
	git diff
	git diff --staged
```
### GIT HEAD

Saca un archivo del commit
```ssh
	git reset HEAD <archivo>
```
Devuelve el ultimo commit que se hizo y pone los cambios en staging
```ssh
	git reset --soft HEAD^
```
Devuelve el ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^
```
Devuelve los 2 ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^^
```
Rollback merge/commit
```ssh
	git log
	git reset --hard <commit_sha>
```
### GIT REMOTE

Agregar repositorio remoto
```ssh
	git remote add origin <url>
```
Cambiar de remote
```ssh
	git remote set-url origin <url>
```
Remover repositorio
```ssh
	git remote rm <name/origin>
```
Muestra lista repositorios
```ssh
	git remote -v
```
Muestra los branches remotos
```ssh	
	git remote show origin
```
Limpiar todos los branches eliminados
```ssh
	git remote prune origin 
```
### GIT BRANCH

Crea un branch
```ssh
	git branch <nameBranch>
```
Lista los branches
```ssh
	git branch
```
Comando -d elimina el branch y lo une al master
```ssh
	git branch -d <nameBranch>
```
Elimina sin preguntar
```ssh
	git branch -D <nameBranch>
```
### GIT TAG

Muestra una lista de todos los tags
```ssh
	git tag
```
Crea un nuevo tags
```ssh
	git tag -a <verison> - m "esta es la versión x"
```
### GIT REBASE

Los rebase se usan cuando trabajamos con branches esto hace que los branches se pongan al día con el master sin afectar al mismo

Une el branch actual con el mastar, esto no se puede ver como un merge
```ssh
	git rebase
```
Cuando se produce un conflicto no das las siguientes opciones:

cuando resolvemos los conflictos --continue continua la secuencia del rebase donde se pauso
```ssh	
	git rebase --continue 
```
Omite el conflicto y sigue su camino
```ssh
	git rebase --skip
```
Devuelve todo al principio del rebase
```ssh
	git reabse --abort
```
Para hacer un rebase a un branch en especifico
```ssh	
	git rebase <nameBranch>
```
### OTROS COMANDOS

Lista un estado actual del repositorio con lista de archivos modificados o agregados
```ssh
	git status
```
Quita del HEAD un archivo y le pone el estado de no trabajado
```ssh
	git checkout -- <file>
```
Crea un branch en base a uno online
```ssh
	git checkout -b newlocalbranchname origin/branch-name
```
Busca los cambios nuevos y actualiza el repositorio
```ssh
	git pull origin <nameBranch>
```
Cambiar de branch
```ssh
	git checkout <nameBranch/tagname>
```
Une el branch actual con el especificado
```ssh
	git merge <nameBranch>
```
Verifica cambios en el repositorio online con el local
```ssh
	git fetch
```
Borrar un archivo del repositorio
```ssh
	git rm <archivo> 
```

### Fork

Descargar remote de un fork
```
	git remote add upstream <url>
```

Merge con master de un fork
```
	git fetch upstream
	git merge upstream/master
```
## NOTAS
Para un mejor desarrollo adjuntamos un enlace a una pagina en la que nos da todas las introducciones rápidas para la introducción al mundo de GitHub así como opciones de descarga.

***[BIENVENIDO AL MUNDO DE GITHUB]***(https://rogerdudler.github.io/git-guide/index.es.html)