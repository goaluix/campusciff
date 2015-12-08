# campusciff
Repositorio para las prácticas del módulo Data Science ToolKit, Máster Executive en Big Data y Business Analytics

### Comandos utilizados y descripción

0. Creo desde github un repositorio llamado campusciff. Además, desde la terminal, creo en mi equipo un directorio llamado ejercicio y accedo a él.

1. Clono el repositorio remoto
```sh
$ git clone git@github.com:goaluix/campusciff.git
```
Salida:
```sh
Cloning into 'campusciff'...
Enter passphrase for key '/c/Users/ico753/.ssh/id_rsa':
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Checking connectivity... done.
```

2. Subo al stage
```sh
$ git add .
```
3. Commit inicial
```sh
$ git commit -m "commit inicial"
```
Salida:
```sh
[master 0253712] commit inicial
 1 file changed, 19 insertions(+)
```

4. Creo archivo y carpeta privada
```sh
$ echo "contraseña 1234" > privado.txt
$ mkdir privada
```

5. Abro el editor vi y creo .gitignore con dos líneas para que se ignoren ese archivo y carpeta

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

git tag v0.1
git push --tag origin master
   
10. Creo rama v0.2 y me posiciono en ella
$ git branch v0.2
$ git checkout v0.2
11. Compruebo que el head apunta a mi nueva rama
$ git log --oneline --decorate --graph --all
* ac67a3e (HEAD -> v0.2, origin/master, origin/HEAD, master) README.md actualizado
* e5f5e49 (tag: v0.1) actulizado README.md
* ef73f30 añadido .gitignore
* 0253712 commit inicial
* 2e5d166 Initial commit

12. Me posiciono de nuevo en master y hago merge con v0.2/2
$ git checkout master
$ git merge v0.2

13. Merge con conflicto
Añado "Hola" a 1.txt
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




