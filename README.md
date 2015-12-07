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
git add .
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



