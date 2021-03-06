# Curso Git
Directorio de prueba para el curso profesional de git github de la plataforma de platzi.

***

# Apuntes del curso

## Comandos basicos

git init &rarr; genera carpeta git que almacena cambios atomicos

git add `file`  			&rarr; agrega archivo modificado al commit  &rarr; trackea el archivo (tracked)

git add . 					&rarr; agrega todos los archivo que hayan sido modificado al commit

git commit -m `mensaje` 	&rarr; comenta cambio

git commit -am 				&rarr; agrega a stagging y hace commit, algo como add + commit, solo se aplica a archivos que se les haya hecho add previamente

git status 					&rarr; indica el estado actual de los archivos

git rm &rarr; borrar

git rm --cache `file`		&rarr; borra el archivo del cache, por tanto ya no se enviara en caso de un push

git rm --force				&rarr; Elimina los archivos de Git y del disco duro. 

git checkout `rama`					&rarr;	trae los cambios de una rama especifica

git checkout `id comit` `file` 		&rarr;	trae los cambios de un archivo de un commit especifico

gat branch 							&rarr; lista las ramas

git branch `rama`					&rarr; Crea una rama nueva

gat branch -r							&rarr; lista las ramas REMOTAS

gat branch -a							&rarr; lista TODAS las ramas

git checkout `rama`					&rarr; te cambias  a la rama

git merge `rama` 					&rarr; mescla la rama actual con la rama indicada

git pull origin master 				&rarr; trae los cambios del origen rama master

git push origin master				&rarr; envia los cambios del origen rama master

git pull origin master --allow-unrelated-histories		&rarr;	 permite hacer pull a origin master fucionando las historias

## Reset y check ramas

git reset `id commit` --soft			&rarr; reset suave, los archivos vuelven a la version del commit, pero el staying se mantiene

git reset `id commit` --hard			&rarr; reset duro, todo vuelve a la versión del commit señalado

git checkout -- `file`                  &rarr; Devuelve un archivo a su estado original en la rama

git rebase `rama`                       &rarr; Trae la historia de una rama y la aplica sobre a rama actual. (Esto solo debe realizarse local)

git clean -f                            &rarr; Borra los archivos inecesarios del espacio de trabajo

git clean --dry-run                     &rarr; Indica que archivos serían borrados en caso de correr git clean

git cherry-pick `id commit`              &rarr; Trae los cambios de un commit viejo, de cualquier rama y los mergea con la rama actual

git commit --amend 		                &rarr; agrega cambio al commit

# stash

git stash                               &rarr; Guarda los cambios    

git stash pop                           &rarr; Trae los cambios del primer elemento de la lista stash 

git stash drop                          &rarr; Borra el elemento posiciona en stash

git stash branch `rama`                        &rarr; envia el primer cambio de la lista stash a la rama, si no existe la crea  

git switch -c `branch`              &rarr; lleva el commit realizado a una nueva rama, si no existe la crea


## Registros

git show `file` 			&rarr; muestra los cambios realizados y la cabecera

git show `file` 			&rarr; muestra los cambios realizados sobre un archivo

git log `file`				&rarr; muestra los commit realizado sobre un archivo junto con su id, sirve para git diff

git log --stat   			&rarr; igual que lo anterior, muestra todos los commit mas los cambios en los archivos

git diff `commit id1` `commit id2` 	&rarr; muestra la diferencia entre dos commit realizados 

git diff								&rarr; muestra diferencia actual con el staying

git reflow                  &rarr; muestra todos los cambios, indepediente si las ramas fueron borradas

git blame `file`             &rarr; muestra todos los cambios realizados sobre un archivo y por quien

git blame `file` -L1,10            &rarr; muestra todos los cambios realizados sobre un archivo solo en las lineas señaladas

## Tag y arboles de registro

git tag -a `nombre tag` `id commit`			    &rarr; Crea un tag para el commit señalado

git tag -d `nombre tag`							&rarr; Borra un tag localmente

git tag -d nombre-del-tag y git push origin :refs/tags/nombre-del-ta       &rarr; Borra un tag en la nube

git tag o git show-ref --tags					&rarr; Muestra los tags creados

git push origin --tags							&rarr; Envia al repositorio en las nuve los tags creados

git log --all --graph --decorate --oneline		&rarr; muestra ramas como linea

git show-branch -all                    &rarr; muestra las ramas que existen con sus commit    

gitk                                    &rarr; interfaz gráfica que muestra las ramas


## Configurar proyecto

git config

git remote add origin `url http ssh`		&rarr; agregar trabajo remoto desde un origen

git remote rm destination					&rarr; borra trabajo remoto desde un origen


git config --list --show-origin 		&rarr;	donde se guardan las configuraciones de git


## Generar SSH
SSH &rarr; SECURE SHELL

ssh-keygen -t rsa -b 4096 -C `mail`
* ssh-keygen 	&rarr; generar key,
* -t rsa 		&rarr; especificar agoritmo rsa 
* -b 4096 	&rarr; que tan compleja la llave 4096 bits!
* -C 			&rarr; que correo



eval $(ssh-agent -s) 							&rarr; evaluar si el agente ssh esta corriendo

ssh-add ruta-donde-guardaste-tu-llave-privada	&rarr; Añadir tu llave SSH a este "servidor":


## Extra

git grep -n `palabra`       &rarr; entrega los archivos y linea donde fueron usada la palabra
git grep -c `palabra`       &rarr; cuenta donde fueron usada la palabra
git log -S `palabra`        &rarr; entrega todos los commit relacionados con la palabra


git shortlog -sn  -all --no-merges
* shortlog          &rarr;  Muestra los commit hechos por cada uno del equipo
* -sn               &rarr;  Muestra los totales
* --all              &rarr;  Incluye commit borrados
* --no-merges       &rarr;  Excluye los merge


git config --global alias.`nombre command`= `command`             &rarr; guarda en la configuracion global de git un comando con un alias
alias `nombre command`= `command`                                 &rarr; crea un alias en el bash asociado al commando

git `command` -help            &rarr; abri la guía de ayuda para indicar como funciona el comando      


