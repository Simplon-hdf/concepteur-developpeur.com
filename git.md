# GIT

- [GIT](#git)
  - [Installation <a name="Installation"></a>](#installation-)
      - [linux :](#linux-)
      - [Mac :](#mac-)
      - [Windows:](#windows)
    - [Principale commande de base :](#principale-commande-de-base-)
    - [Fonctionnement de GIT: <a name="#Commande"></a>](#fonctionnement-de-git-)
      - [Créer un projet à partir d'un dépôt vide](#créer-un-projet-à-partir-dun-dépôt-vide)
  - [Branches](#branches)
  - [Pull request <a name="#Commande"></a>](#pull-request-)
    - [Fonctionnement:](#fonctionnement)
##Introduction<a name="Introduction"></a>
GIT a été créé en 2005 par Linus Torvalds, créateur de LINUX. 
C'est un Logiciel libre, gratuit, permettant de travailler en collabaration et de sauvegarder son travail. Tout en protégeant le code source, il permet de suivre chaque changements apportés, de garder une trace et revenir en arrière si besoin.
Git permet de travailler en local sans nécessité de se connecter à internet. 
  


## Installation <a name="Installation"></a>
#### linux : 
```
sudo dnf install git-all
```
#### Mac : 
  Homebrew:
 ```
  brew install git
 ```
#### Windows: 
[Téléchargez-le](https://git-scm.com/download/win)

### Principale commande de base : 

| Commande | Description |
| ---- | ---- |
| git init | Initialise git dans un dossier|
| git config| Permet de modifier la configuration git en insérant des valeurs à des clés |
| git status | Obtient la liste dans le stage|
| git add | Ajoute un ou plusieurs fichier(s) au stage : vous pouvez choisir de prendre un ou plusieurs fichiers avant de le mettre dans le dépôt local et de le commit|
| git commit | Envoi le fichier dans le dépôt local tout en détaillant les modifications apportés au code|
| git remote | Lie votre dépôt local à votre dépôt distant, permettant d'envoyer votre fichier sur le dépôt distant|
| git push | Permet d'envoyer les changements apportés à votre dépôt local vers le dépôt distant |
| git pull | Lors d'une collaboration met à jour le dépot local depuis le dépôt distant|
| git fetch | Récupère toutes les données des commits effectuées sur la branche courante qui n'existe pas encore en dépôt local |
| git clone | Clone un dépôt distant à partir d'une URL existante(github) vers le dépôt local |
| git branch | Créer une branche |
| git checkout | Change de branche |
| git merge | Fusionne l'historique d'une branche dans la branche actuelle|

![commande de base ](https://blog.freelancerepublik.com/wp-content/uploads/2021/12/Git-Architechture.png)

Le working directory est comme un espace de travail où vous travaillez sur un fichier.
Le staging area est comme une salle d'attente avant que le fichier ne soit indexé par la commande git add.
Le local repo est la validation du fichier par la commande git commit.
Le remote repo est un serveur sur lequelle nous envoyons nos fichiers depuis local repo.
### Fonctionnement de GIT: <a name="#Commande"></a>

#### Créer un projet à partir d'un dépôt vide
 Créer un nouveau dépôt dans Github
```sh
git init 
git branch -M my_branch
git add my_file_name
git commit -m my_commit_message
git remote add origin my_repository_URL
git push -u origin my_branch
```
Si vous voulez add plusieurs dossiers en même-temps :
```
git add .
```
## Branches 
Lors d'un travail à plusieurs, git permet d'identifier chaque modifications, sur un projet commun avec des commits et des branches différentes.
Une branche contient plusieurs commits avec un pointeur, en avançant dans le projet, les commits augmentent sur la branche. 
Travailler sur une branche secondaire permet de ne pas interférer dans le travail de la branche principale et de garder la meilleure version.
Il existe plusieurs branches que l'on peut renommer comme l'on souhaite :  
- La branche par défaut est "master" que l'on doit la renommer en "main". 
- La branche "develop" créer à partir de "main".
- Les branches "feature" à partir de "develop" pour travailler dessus et garder la meilleure version. 
 

```sh
git branch develop  #Créer une branche develop
git checkout develop  #Change sur la branche develop
git branch feature1 
git chekckout feature1 
git checkout develop 
git merge feature1  # fusionne sur la branche develop
git branch -d feature1 # supprime la branche feature1
```
![Les branches](https://uploads.sitepoint.com/wp-content/uploads/2019/06/155993572204-gitflow.png)

## Pull request <a name="#Commande"></a>
Avec une collaboration sur un projet GIT il est nécessaire d'avoir un dépôt distant (Github).
Récupère un projet upstream permettant de travailler en collaboration.
Upstream représente un dépôt distant externe au votre.
Origin réprésente votre dépôt distant.
Fork permet d'aller chercher un dépôt d'upstream vers origin.

![pull request](https://devopscube.com/wp-content/uploads/2021/02/git-forked-upstream-min.png.webp)

### Fonctionnement:
1) Fork un projet upstream vers origin
2) Clone le nouveau projet dans le local
3) Créer une new branche
4) Push ton travail sur origin
5) Proposer son projet à upstream
6) Propiétaire soumet des vérifications à l'upstream