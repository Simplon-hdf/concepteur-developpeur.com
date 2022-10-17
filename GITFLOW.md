# Gitflow

## Sommaire

- [Gitflow](#gitflow)
  - [Sommaire](#sommaire)
  - [Description](#description)
  - [Installation](#installation)
    - [Commande d'installation](#commande-dinstallation)
      - [Mac OS](#mac-os)
        - [Linux](#linux)
        - [Windows](#windows)
    - [Fonctionnement de Gitflow](#fonctionnement-de-gitflow)
    - [Initialisation de gitflow](#initialisation-de-gitflow)

## Description

Cette extension permet de gérer le versioning d'un projet et pose un cadre de travail.
Les développeurs qui travaillent sur un projet géré par Gitflow doivent suivre un Workflow établi et éprouvé.

## Installation

- Une installation fonctionnelle de git est requise
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

Gitflow est un ensemble de règles simples qui se basent sur le fonctionnement par branche de Git.
Gitflow génére de manière automatique de multiple chose dont les branches ==Main== et ==Develop==.
La branche ==Main== est la branche dite principale souvent utilisé lors de la production.
La branche ==Develop== rassemble toutes les fonctionnalitées mais il est recommandé de ne pas faire de modification directement dans cette branche
Il permet de réalisé plusieurs commande git en une seule ligne.

</br>

### Initialisation de gitflow

Pour démarrer l'iniatialisation, lancez la commande :

```
git flow init
```

L'extension propose de préfixer les branches de Gitflow. Il est conseillé de laisser les valeurs par défaut.(appuyer sur entrée à chaque proposition)

</br>
