#Git/Github - démarrage rapide
##1. Installation
Dans le terminal, tapez
```
sudo apt-get install git
```
##2. Configuration
```
git config --global user.name "user_name"
git config --global user.email "email_id"
```
##3. Créer un "repository" (ou repo)
###a. Créer le dossier de votre projet
```
git init MonProjet
```
Ce message devrait apparaître
```
Initialized empty Git repository in /chemin_dossier/MonProjet/.git/
```
###b. Entrer dans le dossier
```
cd MonProjet
```
###c. Créer un fichier readme.md. 
```
git add README.md
```
et ajouter un texte, par exemple "**Ceci est un mon premier repo**"
**.md** = markdown qui peut être mis en page, par exemple là https://stackedit.io/editor
Ce fichier s'ouvre par défaut à l'arrivée sur GitHub
Vous pouvez également ajouter tous les fichiers qui existeraient déjà dans **MonProjet**
###d. Créer un compte sur GitHub
Créer un compte sur https://github.com, puis créer un repository. Il faut lui donner le même nom que celui créé en local avec `git init`. Ici c'est **MonProjet**
###e. Commandes Git
Pour ajouter tous les fichiers (ajoutés, supprimés ou modifiés) 
```
git add --all 
```
Préparer le commit
```
git commit -m "some_message"
```
Les deux commandes précédentes peuvent être en une fois
```
git commit -am "commit message"
```
Pour créer la branche. **user_name** doit correspondre à celui de votre compte sur GitHub. Cette commande n'est à faire qu'une seule fois, tant que l'on reste dans la même branche.
```
git remote add origin https://github.com/user_name/MonProjet.git
```
Pour "pousser" les fichier dans le repo. Grâce à l'option **-u**, on se "connecter" par défaut à cette branche. 
```
git push -u origin master
```
Une fois le premier commit fait, on peut juste faire 
```
git commit -am "commit message"
git pull
git push
```
**git pull** permet de récupérer les changements apportés en ligne - en cas de travail collaboratif par exemple, ou de création d'un fichier en ligne - et de les fusionnés avec la version locale.

Pour éviter de mettre en ligne certains fichiers/dossiers, créer un fichier **.gitignore** dans la racine du projet (ou dans un sous-dossier) et ajouter les exceptions. Ajouter par exemple **vendor/** dans **.gitignore**
