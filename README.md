# campusciff
Repositorio para las prácticas del módulo Data Science ToolKit, Máster Executive en Big Data y Business Analytics

### Comandos utilizados y descripción

0. Creo desde github un repositorio llamado campusciff. Además, desde la terminal, creo en mi equipo un directorio llamado ejercicio y accedo a él.

1. Clono el repositorio remoto

	```sh
	$ git clone git@github.com:goaluix/campusciff.git
	```

2. Subo al stage
	```sh
	$ git add .
	```
3. Commit inicial
	```sh
	$ git commit -m "commit inicial"
	```


4. Creo archivo y carpeta privada
	```sh
	$ echo "contraseña 1234" > privado.txt
	$ mkdir privada
	```

5. Abro el editor vi y creo .gitignore con dos líneas para que se ignoren ese archivo y carpeta
	![alt text](https://github.com/goaluix/campusciff/blob/master/captura_vi.png "Editor vi")
6. Creo 1.txt
	```sh
	$ echo "One" > 1.txt
	```

7. Subo .gitignore y 1.txt
	```sh
	$ git add .
	$ git commit -m "añadido .gitignore"
	```
8. Actualizo README.md
	```sh
	$ git add .
	$ git commit -m "actulizado README.md"
	```

9. Creo y subo etiquetas
	```sh
	$ git tag v0.1
	$ git push --tag origin master
	``` 
10. Creo rama v0.2 y me posiciono en ella
	```sh
	$ git branch v0.2
	$ git checkout v0.2
	$ echo "dos" > 2.txt
	$ git add .
	$ git commit -m "Añadido 2.txt "
	``` 
11. Compruebo que el head apunta a mi nueva rama
	```sh
	$ git log --oneline --decorate --graph --all
	* ac67a3e (HEAD -> v0.2, origin/master, origin/HEAD, master) README.md actualizado
	* e5f5e49 (tag: v0.1) actulizado README.md
	* ef73f30 añadido .gitignore
	* 0253712 commit inicial
	* 2e5d166 Initial commit
	$ git push origin v0.2
	``` 
12. Me posiciono de nuevo en master y hago merge con v0.2
	```sh
	$ git checkout master
	$ git merge v0.2
	``` 

13. Merge con conflicto. 
	```sh
	$ echo "Hola" >> 1.txt
	$ git add .
	$ git commit -m "añadido hola a 1.txt"
	$ git checkout v0.2

	$ echo "adios" > 1.txt
	$ git add .
	$ git commit -m "añadido adios a 1.txt (v0.2)"

	$ git checkout master
	$ git merge v0.2
	Auto-merging 1.txt
	CONFLICT (content): Merge conflict in 1.txt
	Automatic merge failed; fix conflicts and then commit the result.

	$ cat 1.txt
	<<<<<<< HEAD
	One
	Hola
	=======
	adios
	>>>>>>> v0.2

	$ vi 1.txt
	$ cat 1.txt
	One
	Hola y adios

	$ git add .
	$ git commit -m "conflicto resuelto entre master y v0.2"
	$ git push origin master
	```
14. Creo etiqueta v0.2
	```sh
	$ git tag v0.2
	```
15. Elimino rama v0.2 (en local, para remoto habría que usar además git push alias-repositorio-remoto --delete nombre-rama-remota)
	```sh
	$ git branch -d v0.2
	```
16. Listo los distintos commits
	```sh
$ git log --oneline --decorate --graph --all
* 0d4efd1 (HEAD -> master, origin/master, origin/HEAD) README.md formateado
* 5ae73f0 README.md actualizado
*   f7b1d43 (tag: v0.2) conflicto resuelto entre master y v0.2
|\
| * 25dd144 añadido adios a 1.txt (v0.2)
* | 8befef5 añadido hola a 1.txt
|/
* 03a4977 (origin/v0.2) Añadido 2.txt
* ac67a3e README.md actualizado
* e5f5e49 (tag: v0.1) actulizado README.md
* ef73f30 añadido .gitignore
* 0253712 commit inicial
* 2e5d166 Initial commit
	```
	
17. Poner foto en el perfil. Desde la opción de profile
	![alt text](https://github.com/goaluix/campusciff/blob/master/fotosubida.jpg "Profile github")

18. Doble factor de autenticación. 
	![alt text](https://github.com/goaluix/campusciff/blob/master/auth1.png "Autenticación")
	Eligo sms. Github envía un código para validar.
	![alt text](https://github.com/goaluix/campusciff/blob/master/auth2.png "Autenticación por sms")
	Activado el doble factor de seguridad
	![alt text](https://github.com/goaluix/campusciff/blob/master/auth3.png "Doble factor")

19. Clave pública. Ya estaba añadida
	![alt text](https://github.com/goaluix/campusciff/blob/master/ssh.png "ssh")
	
20. Tabla con compañeros
	Nombre | Github
	------- | -------
	MiguelCerdan | https://github.com/MiguelCerdan/campusciff.git
	adiazgalache | https://github.com/adiazgalache/campusciff.git
	macarenagaranena| https://github.com/macarenagaranena/campusciff.git
	plopez76 | https://github.com/plopez76/campusciff.git

21. 

	
