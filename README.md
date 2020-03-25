# cursoGit
Directorio de prueba para el curso profesional de git github de la plataforma de platzi.


#Apuntes del curso

## Comandos basicos

git init => genera carpeta git que almacena cambios atomicos


git add <file>  			=> agrega archivo modificado al commit  => trackea el archivo (tracked)
git add . 					=> agrega todos los archivo que hayan sido modificado al commit
git commit -m <mensaje>		=> comenta cambio

git commit -am 				=> agrega a stagging y hace commit, algo como add + commit, solo se aplica a archivos que se les haya hecho add previamente

git status 					=> indica el estado actual de los archivos

git rm => borrar
git rm --cache <file>		=> borra el archivo del cache, por tanto ya no se enviara en caso de un push
git rm --force				=> Elimina los archivos de Git y del disco duro. 


git checkout <rama>					=>	trae los cambios de una rama especifica
git checkout <id comit> <file> 		=>	trae los cambios de un archivo de un commit especifico

gat branch 							=> lista las ramas
git branch <rama>					=> Crea una rama nueva
git checkout <rama>					=> te cambias  a la rama

git merge <rama> 					=> mescla la rama actual con la rama indicada

git pull origin master 				=> trae los cambios del origen rama master
git push origin master				=> envia los cambios del origen rama master
git pull origin master --allow-unrelated-histories		=>	 permite hacer pull a origin master fucionando las historias

## Reset y swing ramas

git reset <id commit> --soft			=> reset suave, los archivos vuelven a la version del commit, pero el staying se mantiene
git reset <id commit> --hard			=> reset duro, todo vuelve a la versión del commit señalado

git switch -c <new-branch-name>




## Registros

git show <file> 			=> muestra los cambios realizados y la cabecera
git show <file> 			=> muestra los cambios realizados sobre un archivo
git log <file>				=> muestra los commit realizado sobre un archivo junto con su id, sirve para git diff
git log --stat   			=> igual que lo anterior, muestra todos los commit mas los cambios en los archivos

git log --all --graph --decorate --oneline		=> muestra ramas como linea
alias arbol =""


git diff <commit id1 > <commit id2> 	=> muestra la diferencia entre dos commit realizados 
git diff								=> muestra diferencia actual con el staying

## Configurar proyecto

git config

git remote add origin <url http ossh>		=> agregar trabajo remoto desde el origen
git remote rm destination					=> borra trabajo remoto desde origen


git config --list --show-origin 		=>	donde se guardan las configuraciones de git



## Generar SSH
SSH => SECURE SHELL

ssh-keygen -t rsa -b 4096 -C <mail>
	ssh-keygen 	=> generar key,
	-t rsa 		=> especificar agoritmo rsa 
	-b 4096 	=> que tan compleja la llave 4096 bits!
	-C 			=> que correo



eval $(ssh-agent -s) 							=> evaluar si el agente ssh esta corriendo

ssh-add ruta-donde-guardaste-tu-llave-privada	=> Añadir tu llave SSH a este "servidor":











