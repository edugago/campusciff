# Practica git y github campusciff Edugago	
## 2.1 Repositorio Campusciff
Creo el repositorio campusciff desde la web de github

```sh
git clone git@github.com:edugago/campusciff.git
```

## 2.2 Readme
README.md ya creado desde la web de github, incluyo algunos cambios para subirlo

```sh
echo "git clone git@github.com:edugago/campusciff.git" >> README.md
git add README.md
```

## 2.3 Commit y push inicial
```sh
git commit -m "commit inicial"
git push origin master 
```

## 2.4 Ignorar archivos
```sh
echo privado > privado.txt
mkdir privada
echo "privado.txt" > .gitignore
echo privada >> .gitignore
```

## 2.5 Crear tag
```sh
echo 1 >> 1.txt
git add 1.txt
git commit -m "subida la parte del tag"
git tag v0.1
git push origin master
```

## 2.6 Crear rama
```sh
git branch v0.2
git checkout v0.2
git log --oneline --decorate --graph --all
echo 2 > 2.txt
git add 2.txt
git commit -m "subo 2.txt a la rama v0.2"
git push origin v0.2:v0.2
```

## 2.7 Merge directo
```sh
git checkout master
git merge v0.2
```
Como tengo cambios hechos en README.md en la rama, me dice que el contenido va a ser sobreescrito en master (conflictos)

## 2.8 Merge con conflicto
```sh
echo Hola >> 1.txt
git add 1.txt
git commit -m "commit merge conflicto 1"
git checkout v0.2
echo Adios >> 1.txt
git add 1.txt
git commit -m "commit merge conflicto 2"
git checkout master
git merge v0.2
git branch --merged
git branch --no-merged
```

La rama figura como no merged porque aun está el conflicto sin resolver

Edito los conflictos del fichero y lo guardo de nuevo

```sh
git commit -am "commit merge conflicto 3"
git merge v0.2
```

Ahora el commando ya dice que up-to-date

## 2.9 Borrar rama
```sh
git tag v0.2
git log --oneline --decorate --graph --all
git branch -d V0.2
```

## 2.10 Cuenta de Github

Pongo la foto desde la web de github

Activo el doble factor de autenticación

Las claves ya las tenia importadas previamente

## 2.11 Uso social de Github
Añado watch a unos cuantos compañeros de clase, tambien les marco con unas estrella

## 2.12 Crear una tabla
|        NOMBRE       |                GITHUB                | 
|:--------------------|:-------------------------------------|
| Macarena Garañena | **https://github.com/macarenagaranena** |   
| Miriam Garcia  |   **https://github.com/Miriam-Asenjo**   |  
| Daniel Escuder  |     **https://github.com/Danielobit**     | 
| Luis Nuño |     **https://github.com/goaluix**     |   


## 2.13 Colaboradores

Añado a github.com/asanzdiego como colaborador

## 2.14 Crear una organización

Creo una organizacion llamada campusciff-edugago

## 2.15 Crear equipos

Creo los equipos de administradores y colaboradores y envio invitaciones a asanzdiego y algunos compañeros de clase

## 2.16 Index.html

Creo un index html.

Creo un nuevo repositorio llamado campusciff-edugago.github.io

Subo index.html a ese repositorio

```sh
git clone git@github.com:campusciff-edugago/campusciff-edugago.github.io.git
git add index.html
git commit -m "commit del index"
git push origin master
```
Ahora ya es accesible desde http://campusciff-edugago.github.io/

## 2.17 Pull requests

Hay un fork de campusciff-goaluix.github.io.git

Hago un clone dentro de mi repositorio local de git

```sh
git clone git@github.com:edugago/campusciff-goaluix.github.io.git
git branch v2
git checkout v2
git log --oneline --decorate --graph --all
```
Modifico index.html desde un editor de texto

```sh
git add index.html
git commit -m "subo los cambios de la rama"
git push origin v2
```
