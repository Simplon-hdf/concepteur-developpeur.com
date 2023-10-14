![!](https://res.cloudinary.com/jerrick/image/upload/f_jpg,fl_progressive,q_auto,w_1024/60cba00bd11dde001d9e55c0.png)

## Sommaire

---

<!-- TOC -->

- [Sommaire](#sommaire)
- [Description](#description)
- [Installation](#installation)
  - [Commande d'installation](#commande-dinstallation)
    - [Mac OS](#mac-os)
      - [Linux](#linux)
      - [Windows](#windows)
  - [Fonctionnement de Gitflow](#fonctionnement-de-gitflow)
  - [Initialisation de gitflow](#initialisation-de-gitflow)
  - [Créer une fonctionnalité](#créer-une-fonctionnalité)
    - [Terminer une fonctionnalité](#terminer-une-fonctionnalité)
  - [Commencer une Livraison/release](#commencer-une-livraisonrelease)
    - [Terminer une livraison](#terminer-une-livraison)
  - [Commencer un correctif](#commencer-un-correctif)
    - [Terminer un correctif](#terminer-un-correctif)
- [Références](#références)
<!-- TOC -->

## Description

---

Cette extension permet de traiter le versioning d'un projet et pose un cadre de travail.
Les développeurs qui travaillent sur un projet géré par Gitflow doivent suivre un Workflow établi et éprouvé.

## Installation

---

- Une installation fonctionnelle de Git est requise
- Gitflow fonctionne sur macOS, Linux et Windows

### Commande d'installation

#### Mac OS

_Homebrew_

```
brew install git-flow-avh
```

##### Linux

```
apt-get install git-flow
```

##### Windows

Sous Windows, vous devrez télécharger et installer git-flow.
[Installation GitFlow](https://git-scm.com/download/win)

### Fonctionnement de Gitflow

---

![!](https://wac-cdn.atlassian.com/dam/jcr:a13c18d6-94f3-4fc4-84fb-2b8f1b2fd339/01%20How%20it%20works.svg?cdnVersion=584)

Gitflow est un ensemble de règles simples qui se basent sur le fonctionnement par branche de Git.
Gitflow génére de manière automatique de multiple chose dont les branches ==Main== et ==Develop==.
La branche ==Main== est la branche dite principale souvent utilisée lors de la production.
La branche ==Develop== rassemble toutes les fonctionnalités, mais il est recommandé de ne pas faire de modification directement dans cette branche
Il permet de réaliser plusieurs commandes git en une seule ligne.

### Initialisation de gitflow

---

Pour lancer l'initialisation, lancez la commande :

```
git flow init
```

L'extension propose de préfixer les branches de Gitflow. Il est conseillé de laisser les valeurs par défaut.(appuyer sur entrée à chaque proposition)

### Créer une fonctionnalité

---

![!](https://wac-cdn.atlassian.com/dam/jcr:34c86360-8dea-4be4-92f7-6597d4d5bfae/02%20Feature%20branches.svg?cdnVersion=584)

Pour gitflow créer une fonctionnalité correspond à la création d'une nouvelle branche de type ==feature==.Cela permet de développer plusieurs fonctionnalités en parallèle, souvent utilisé pour le travail en équipe.

Pour créer une fonctionnalité, lancer la commande :

```
git flow feature start Myfeature
```

Cette commande créer une branche et se positionne sur celle-ci.

**Commande correspondante sur Git :**

```
git checkout develop
git checkout -b feature/Myfeature
```

#### Terminer une fonctionnalité

Lorsque votre fonctionnalité est finie, vous devez lancer la commande :

```
git flow feature finish Myfeature
```

Gitflow retourne sur la branche ==Develop== et merge la branche ==feature==/Myfeature, une fois le merge réussi la branche est supprimée.

**Commande correspondante sur Git :**

```
git checkout develop
git merge feature/Myfeature
git branch -D feature/Myfeature
```

### Commencer une Livraison/release

---

![!](https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=584)

Gitflow permet aussi de gérer les versions avec la création de branche ==release==, pouvant être utilisé lors de la production.

Pour créer une version lancer la commande :

```
git flow release start 1.0.0
```

L'extension crée une branche ==release== en se plaçant sur la branche ==Develop==.

#### Terminer une livraison

Après avoir effectué les actions voulues, vous devez lancer la commande :

```
git flow release finish 1.0.0
```

Cette commande merge la branche ==release== à la branche ==main==.

**Commande correspondante sur Git :**

```
git checkout main
git merge release/1.0.0
```

### Commencer un correctif

---

![!](https://wac-cdn.atlassian.com/dam/jcr:cc0b526e-adb7-4d45-874e-9bcea9898b4a/04%20Hotfix%20branches.svg?cdnVersion=584)

En cas d'erreur lors de la production, la création d'une branche ==hotfix== peut être créé.
Pour cela lancer la commande :

```
git flow hotfix start myBranch
```

Cette commande crée une branche à partir de la branche ==main==.

**Commande correspondante sur Git :**

```
git checkout main
git checkout -b hotfix/myBranch
```

#### Terminer un correctif

Lorsque votre ==hotfix== est terminé lancer la commande :

```
git flow hotfix finish myBranch
```

Cette commande envoie les changements à la fois sur la branche ==main== et la branche ==Develop==.

**Commande correspondante sur Git :**

```
git checkout master
git merge hotfix/myBranch
git checkout develop
git merge hotfix/myBranch
git branch -D hotfix/myBranch
```

## Références

---

- [Explication du modèle](https://nvie.com/posts/a-successful-git-branching-model/) (Auteur de gitflow)

- [Cheat Sheet](http://danielkummer.github.io/git-flow-cheatsheet/index.fr_FR.html)

- [Tutoriel](https://jeffkreeftmeijer.com/git-flow/)

- [Tutoriel vidéo](https://www.youtube.com/watch?v=ZQAQ4HcskAY)
