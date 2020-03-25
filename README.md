# Curso Git
Directorio de prueba para el curso profesional de git github de la plataforma de platzi.

***

# Apuntes del curso

## Comandos basicos

git init &rarr; genera carpeta git que almacena cambios atomicos


git add <file>  			&rarr; agrega archivo modificado al commit  &rarr; trackea el archivo (tracked)

git add . 					&rarr; agrega todos los archivo que hayan sido modificado al commit

git commit -m <mensaje>		&rarr; comenta cambio

git commit -am 				&rarr; agrega a stagging y hace commit, algo como add + commit, solo se aplica a archivos que se les haya hecho add previamente

git status 					&rarr; indica el estado actual de los archivos

git rm &rarr; borrar

git rm --cache <file>		&rarr; borra el archivo del cache, por tanto ya no se enviara en caso de un push

git rm --force				&rarr; Elimina los archivos de Git y del disco duro. 


git checkout <rama>					&rarr;	trae los cambios de una rama especifica

git checkout <id comit> <file> 		&rarr;	trae los cambios de un archivo de un commit especifico

gat branch 							&rarr; lista las ramas

git branch <rama>					&rarr; Crea una rama nueva

git checkout <rama>					&rarr; te cambias  a la rama

git merge <rama> 					&rarr; mescla la rama actual con la rama indicada

git pull origin master 				&rarr; trae los cambios del origen rama master

git push origin master				&rarr; envia los cambios del origen rama master

git pull origin master --allow-unrelated-histories		&rarr;	 permite hacer pull a origin master fucionando las historias

## Reset y swing ramas

git reset <id commit> --soft			&rarr; reset suave, los archivos vuelven a la version del commit, pero el staying se mantiene

git reset <id commit> --hard			&rarr; reset duro, todo vuelve a la versión del commit señalado

git switch -c <new-branch-name>




## Registros

git show <file> 			&rarr; muestra los cambios realizados y la cabecera

git show <file> 			&rarr; muestra los cambios realizados sobre un archivo

git log <file>				&rarr; muestra los commit realizado sobre un archivo junto con su id, sirve para git diff

git log --stat   			&rarr; igual que lo anterior, muestra todos los commit mas los cambios en los archivos

git diff <commit id1 > <commit id2> 	&rarr; muestra la diferencia entre dos commit realizados 

git diff								&rarr; muestra diferencia actual con el staying


## Tag y arboles de registro

git tag -a <nombre tag> <id commit> 			&rarr; Crea un tag para el commit señalado

git tag -d <nombre tag>							&rarr; Borra un tag

git tag o git show-ref --tags					&rarr; Muestra los tags creados


git push origin --tags							&rarr; Envia al repositorio en las nuve los tags creados

git log --all --graph --decorate --oneline		&rarr; muestra ramas como linea

alias arbol =""



## Configurar proyecto

git config

git remote add origin <url http ossh>		&rarr; agregar trabajo remoto desde el origen

git remote rm destination					&rarr; borra trabajo remoto desde origen


git config --list --show-origin 		&rarr;	donde se guardan las configuraciones de git



## Generar SSH
SSH &rarr; SECURE SHELL

ssh-keygen -t rsa -b 4096 -C <mail>
	* ssh-keygen 	&rarr; generar key,
	* -t rsa 		&rarr; especificar agoritmo rsa 
	* -b 4096 	&rarr; que tan compleja la llave 4096 bits!
	* -C 			&rarr; que correo



eval $(ssh-agent -s) 							&rarr; evaluar si el agente ssh esta corriendo

ssh-add ruta-donde-guardaste-tu-llave-privada	&rarr; Añadir tu llave SSH a este "servidor":











