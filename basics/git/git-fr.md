## Tables des matières

- [Tables des matières](#tables-des-matières)
- [Introduction](#introduction)
- [Installation ](#installation-)
- [Windows](#windows)
- [Mac](#mac)
- [Linux](#linux)
  - [Avec APT](#avec-apt)
  - [Avec Pacman](#avec-pacman)
- [Prise en main](#prise-en-main)
  - [Commandes](#commandes)
  - [Créer un dépôt vide](#créer-un-dépôt-vide)
  - [Branches](#branches)

## Introduction<a name="Introduction"></a>

Git est un logiciel libre (License GNU) et gratuit ayant été crée en 2005 par Linus Torvals (Le créateur de Linux).

Il est utilisé pour versionner son code et permettre à ses utilisateurs de collaborer facilement sur un projet.

Git permet de partager son code avec une équipe (en corrélation avec d'autres plateformes/services), de plus, Git n'a pas besoin de connexion Internet pour fonctionner.

## Installation <a name="Installation"></a>

## Windows

Pour installer Git sous Windows, vous pouvez [le télécharger ici](https://git-scm.com/download/win)

## Mac

Pour Mac, en utilisant `Homebrew`

```sh
brew install git
```

## Linux

Pour Linux, cela dépends de votre gestionnaire de paquet (en fonction de votre distribution)

### Avec APT

```sh
sudo apt-get install git
```

### Avec Pacman

```sh
sudo pacman -S git
```

## Prise en main

### Commandes

| Commande                                       | Description                                                                                                                                                       |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| git init                                       | Créer un dossier .git pour git dans le dossier dans lequel la commande a été exécutée                                                                             |
| git config                                     | Permet de modifier la configuration git dans le dépôt actuel                                                                                                      |
| git status                                     | Affiche le statut de la zone stage, avec chaque fichier ayant subi des modifications, ainsi que chaque fichier modifié qui ne se trouve pas dans la zone de stage |
| git add <nom_du_fichier>                       | Ajoute le(s) fichier(s) spécifié(s) à la zone de stage                                                                                                            |
| git commit                                     | Envoi le contenu de la zone de stage dans le dépôt local                                                                                                          |
| git remote -add <alias> <uri_du_dépôt_distant> | Lie votre dépôt local à un dépôt distant                                                                                                                          |
| git push <alias_du_dépôt_distant>              | Permet d'envoyer les modifications qui ont fait l'objet d'un commit sur le dépôt distant                                                                          |
| git pull <alias_du_dépôt_distant>              | Récupère les modifications du dépôt distant vers le dépôt local                                                                                                   |
| git fetch <alias_du_dépôt_distant>             | Récupére toutes les modifications du dépôt distant (comme les branches et les commits)                                                                            |
| git clone <uri_du_dépôt_distant>               | Récupère un dépôt distant complet et le transfère dans un dossier nommé comme le depôt distant                                                                    |
| git branch <nom_de_la_branche>                 | Créer une branche                                                                                                                                                 |
| git checkout <nom_de_la_branche>               | Change de branche                                                                                                                                                 |
| git merge <nom_de_la_branche_à_fusionner>      | Fusionne les modifications de la branche visée avec celles de la branche sur laquelle vous vous trouvez                                                           |

![commande de base ](https://blog.freelancerepublik.com/wp-content/uploads/2021/12/Git-Architechture.png)

Le working directory est comme un espace de travail où vous travaillez sur un fichier.
Le staging area est comme une salle d'attente avant que le fichier ne soit indexé par la commande git add.
Le local repo est la validation du fichier par la commande git commit.
Le remote repo est un serveur sur le quelle nous envoyons nos fichiers depuis local repo.

### Créer un dépôt vide
ë
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

### Branches

Lors d'un travail à plusieurs, git permet d'identifier chaque modification, sur un projet commun avec des commits et des branches différentes.
Une branche contient plusieurs commits avec un pointeur, en avançant dans le projet, les commits augmentent sur la branche.
Travailler sur une branche secondaire permet de ne pas interférer dans le travail de la branche principale et de garder la meilleure version. Il existe plusieurs branches que l'on peut renommer comme l'on souhaite :
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
