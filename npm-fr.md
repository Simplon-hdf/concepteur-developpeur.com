# Sommaire <a id='summary-fr'></a>

- <a href='#whats-npm-fr'>Introduction a NPM</a>
- - <a href='#whats-npx-fr'>Introduction d'NPX</a>
- <a href='#whats-packages-fr'>Les paquets Node</a>
- <a href='#node-modules-fr'>Les modules Node</a>
- <a href='#package-json-fr'>Le fichier **package.json**</a>
- <a href='#semantic-versionning-fr'>**Le versionnement sémantique**</a>
- <a href='#diff-dependencies-fr'>Difference entre dependencies et devDependencies</a>
- <a href='#package-lock-fr'>Package-lock.json</a>
- <a href='#sources-fr'>Sources</a>

# Qu'est ce que NPM (Node Package Manager) <a id='whats-npm-fr'></a>

NPM est un manager de paquet Node utilisé pour télécharger et publier des paquets Node avec les autres developpeurs qui utilisent NPM<br>
NPM se divisent en 3 grands axes :

1. Le site NPM

    Le site [NPM](https://www.npmjs.com/) sert à connaitre les paquets Node disponibles sur le Registry NPM.

2. CLI ou l’Interface en Ligne de Commande

    La CLI est une énorme partie du NPM puis-ce que c'est par le CLI que vous interagissiez avec NPM et avec le Registry NPM afin<br> de télécharger des paquets s'y trouvant ou de publier 
    vos paquets.

3. NPM Registry ou l'Enregisteur

    Le Registry NPM est en fait une enorme base de donnée qui va contenir des 
    applications prêtes à l'emploi,<br> ou simplement des paquets Node que vous pourrez télécharger afin de les utiliser ou les adapter à vos besoins pour les utiliser dans votre paquet.

## Qu'est ce qu'NPX (Node Package Executer) <a id='whats-npx-fr'></a>

Comme NPM est un gestionnaire de paquet Node, NPX est en faite un executeur des paquets Node
grace à NPX il vous sera possible d'exécuter des paquets Node directement depuis le Registry de NPM.<br>
NPX vous permettra ainsi de ne pas avoir à télécharger au préalable le paquet Node pour l'exécuter<br>

<br>

# Node Package ou Paquet Node <a id='whats-packages-fr'></a>

Un package node est un fichier ou un dossier décrit par un fichier **package.json**.<br>
Le fichier **package.json** va donner des informations à propos de votre package, c'est pourquoi il faut que ce fichier contienne les informations les plus détaillées possible.<br>
Un package node peut être public ou bien privé [En savoir plus sur la visibilité des packages](https://docs.npmjs.com/about-private-packages), comme il peut être restreint à une certaine portée ou non [En savoir plus sur la portée des packages](https://docs.npmjs.com/about-scopes) 

Un package node peut être tout ce qui suit (Et bien plus encore) :

1. Un fichier ou un dossier décrit par un fichier **package.json**
2. Un fichier compressé contenant (1.)
3. Une URL pointant vers 2.
4. L'url d'un repos GitHub qui lorsque cloné donnera un fichier ou un dossier décrit par un fichier **package.json**

<br>

# Node Modules <a id='node-modules-fr'></a>

Un module Node est une dépendance dont votre package aura besoin pour s'exécuter ou simplement qui vous sera nécessaire pour le développement de votre package.<br>

Un module Node peut être :

- Un dossier (Structuré comme un Package)
- Un fichier JS

Vous pouvez voir les module node dans le dossier ``` node_modules ```.<br>
Note : Il se peut qu'un module node ne se soit pas correctement installé, dans ce cas, il est conseillé de supprimer le dossier ``` node_modules ``` et de réinstaller tous les modules.<br>

Puis-ce qu'une image vaut mieux que mille mots :

![](https://guillaume-richard.fr/wp-content/uploads/2020/06/node-modules-app-performance.png)

<br>

Cette image explique à quel point les modules nodes sont une charge importante.<br>
Note : Il est très important de ne pas omettre le ``` node_modules ``` dans votre .gitignore afin de ne pas envoyer tous les modules sur votre dêpot distant.<br>

# **package.json** <a id='package-json-fr'></a>

Comme expliqué plus haut, le fichier **package.json** est un fichier qui est essentiel à votre package Node.<br>
Ce fichier fait office de carte pour votre package, vous aller renseignez beaucoup d'informations dans ce fichier.<br>
Vous pourrez y mettre toutes les informations qui suivent (Et bien plus encore, liste non exhaustive) :

- name : Le nom de votre package
- version : La version de votre package
- description : La description de votre package
- keywords : Ce champ est plutôt optionnel, cependant, si vous voulez partager votre package, il pourrait se révéler indispensable
- homepage : Il peut s'agir d'un dépôt GitHub ou simplement un site, il s'agit simplement de la page de référence liée à votre package
- bugs : Ce champ permet de renseigner ou remonter les bugs liés à votre package
- author : Quelques informations à propos de vous
- main : Permet de définir le point d’entrée de votre package (Habituellement index.js)
- scripts : Permet une configuration avancée pour votre package [En savoir plus sur les valeurs possibles de script](https://docs.npmjs.com/cli/v8/using-npm/scripts)
- dependencies : Ce champ permet de renseigner une liste de dépendances dont votre package aura besoin afin de s’exécuter correctement, son format est le suivant : ``` "express":"4.18.3" ``` permettra de définir que votre package necessitera express en version ``` 4.18.3 ```
- devDependencies : Ce champ permet de renseigner une liste de dépendances necessaires au développement de votre package
- private : Renseigner ce champ permet de s'assurer que votre package ne sera pas publié. Il s'agit d'un booléen

NPM se chargera de générer des valeurs par défaut à des champs non renseignés, par exemple pour le champ ``` script ```.<br>
NPM initialisera le champ avec une valeur de test.

# Semantic Versioning ou Le versionnement sémantique <a id='semantic-versionning-fr'></a>

Le versionnement sémantique est un standard que vous devez suivre lors de modifications significatives de votre package.<br>
Il est recommandé de publier vos modifications avec différentes versions de votre package, champ ``` version ``` de votre **package.json**.<br>
De ce fait, les autres développeurs utilisant votre package pourront comprendre l'étendue des modifications apportées pour chaque version de votre package.<br>
Pour aborder ce qui suit, vous devez comprendre quelques termes :

1. MAJOR : On appellera MAJOR une version qui ne sera pas rétrocompatible
2. MINOR : On appellera MINOR une version qui modifiera votre code (Ajout d'une fonctionnalité par exemple) mais qui restera rétrocompatible
3. PATCH : On appellera PATCH une version qui aura pour effet direct de corriger des bugs, tout en restant rétrocompatible

Recommandation : [Apprenez en plus sur les spécificités du Semantic Versioning](https://semver.org/)

Voici les spécificités globales du versionnement sémantique : 

- Il est recommandé de commencer le développement de votre package en version ``` 1.0.0 ```
- Lorsque vous voudrez faire une mise à jour PATCH, votre package passera en version ``` 1.0.1 ```
- Lorsque vous voudrez faire une mise à jour MINOR, votre package passera en version ``` 1.1.0 ``` comme vous pouvez le constater, le nombre de patch a été remis à 0.
- Lorsque vous voudrez faire une mise à jour MAJOR, votre package passera en version ``` 2.0.0 ``` comme vous pouvez le constater, le nombre de minor a été remis à 0.

Il est important de comprendre que lorsque vous sortez une mise à jour MAJOR, elle influe sur les MINOR ainsi que sur les versions PATCH.<br>
Que lorsque vous sortez une mise à jour MINOR, elle influe sur les versions PATCH.<br>
Note: Chaque chiffre n'est pas limité à 9, une version telle que ``` 2.3.19 ``` est une version totalement correcte.<br>

Afin d'appronfondir sur le sujet, vous pouvez [cliquer ici](https://docs.npmjs.com/about-semantic-versioning#using-semantic-versioning-to-specify-update-types-your-package-can-accept)

# Difference entre ``` dependencies ``` et ``` devDependencies ``` <a id='diff-dependencies-fr'></a>

Le champ ``` dependencies ``` vous permettra de lister les dépendances dont votre package aura besoin pour s'exécuter.<br>
Le champ ``` devDependencies ``` quant à lui vous permettra de lister les dépendances dont vous aurez besoin afin de développer votre package.<br>

Si vous voulez cuisiner un gâteau par exemple et le manger :

Pour la préparation de votre gâteau, vous pourrez utiliser un batteur électrique ou simplement utiliser une fourchette.<br>
Dans cet exemple, le batteur électrique représente une devDependencies, utile, mais optionnel puis-ce qu'il vous est possible d'utiliser une fourchette.<br>
Et la fourchette représente elle, à la fois une devDependencies ainsi qu’une dépendance puisque vous pourrez utiliser cette même fourchette pour manger votre gâteau.<br>

# package-lock.json <a id='package-lock-fr'></a>

Le fichier **package-lock.json**  est automatiquement généré par NPM lorsqu’une opération affectant l'arborescence du dossier ``` node_modules ``` ou le fichier ``` package.json ``` par NPM est effectuée.<br>
Le **package-lock.json** va contenir une description exacte de l'arborescence des dépendances.<br>
Ce fichier est prévu pour être inclus au dêpôt, il peut être utilisé pour :

- Obtenir une seule définition de l'arborescence des dépendances, de cette façon tous les aspects de l'intégration continue sont assurés d'installer les mêmes dépendances.
- Obtenir un moyen simple de retracer les états du ``` node_modules ```
- Obtenir une meilleure visibilité des changements apportés à l'arborescence
- Optimiser l'installation des dépendances, afin de ne pas avoir à re-télécharger les dépendances déjà installées.

Le format du fichier **package-lock.json** ressemble fortement à celui du **package.json**, [En apprendre plus sur le format du **package-lock.json**](https://docs.npmjs.com/cli/v8/configuring-npm/package-lock-json)

# Sources <a id='sources-fr'></a>

Disclaimer : Les sources ci-dessous sont exclusivement en anglais.<br>

- [Qu'est ce que NPM](https://www.w3schools.com/whatis/whatis_npm.asp)
- [Introduction à NPX](https://www.geeksforgeeks.org/what-are-the-differences-between-npm-and-npx/)
- [Module Node & Paquet Node](https://docs.npmjs.com/about-packages-and-modules)
- [Le fichier **package.json**](https://docs.npmjs.com/cli/v8/configuring-npm/package-json)
- [Le versionnement sémantique avec Node](https://docs.npmjs.com/about-semantic-versioning)
- [Le versionnement sémantique](https://semver.org/)
- [La différence entre les champs ``` dependencies ``` et ``` devDependencies ```](https://stackoverflow.com/questions/18875674/whats-the-difference-between-dependencies-devdependencies-and-peerdependencies)
- [Le fichier **package-lock.json**](https://docs.npmjs.com/cli/v8/configuring-npm/package-lock-json)


# Les commandes NPM

# Comment initialiser un projet avec NPM ?

> **npm init**

Le npm init va créer un fichier **package.json** qui va permettre d'obtenir des informations sur son projet.

### Comment installer des modules ?

- ##### Pour pouvoir ajouter un nouveau package à son projet il faudra utiliser :

**Exemple :**

> **npm install express**
OR 
> **npm i express**

 

- ##### Pour pouvoir installer les package déjà existants il faudra utiliser :

> **npm install**
OR
**npm i**

Cette commande va permettre d'installer tous les packages et modules qui ont été ajoutés au projet dans le fichier **package.json**.

- ##### Vous pouvez télécharger une version spécifique d'un package pour revenir à une version antérieure, il vous faudra donc utiliser :

**Exemple :**

> **npm install express@1.0.2**

### Comment installer les package de dépendance de développement ?

- ##### Pour installer les outils qui ne seront utilisés que dans l’environnement de développement, il faudra utiliser :

##### Exemple : 

> **npm install nodemon --save-dev**

Il y aura donc dans le fichier **package.json** le **devDepencies** qui va être ajouté.

### Comment lister des packages installés au projet ?

- Pour lister les packages, au niveau local, il faudra utiliser la commande : 
> **npm list**

OR

> **npm ls**

### Obtenir des informations sur un package

- Pour obtenir des informations sur un package, il faudra utiliser :
> npm **view express**

- Pour obtenir la documentation du package, il faudra utiliser :
> npm **docs express**

### Quels sont les commandes pour faire les mises à jour de NPM ?

**IMPORTANT** : Il faut toujours vérifier que les modules et les packages sont à jours.

- ##### Que faire avant de mettre à jour un package NPM ?

- Avant de mettre à jour **les paquets NPM** il faut regarder si un package est expiré, il faudra alors utiliser : 

> npm **outdated**

Il faudra utiliser la commande depuis le répertoire racine.

#### Il y a deux types d'update :

- Pour mettre à jour tous les packages du projet, il faudra utiliser :

> npm **update**

- Pour mettre à jour un package en particulier, il faudra utiliser : 

> npm **update express**

#### Mettre à jour la nouvelle version NPM :
- Pour mettre à jour la nouvelle version de NPM, il faudra utiliser : 
> npm **install npm@latest -g**

#### Mettre à jour les package de développement :
- Pour mettre à jour un package en DevDepencies, il faudra utiliser :
> npm **update --dev**

### Quels sont les commandes pour désinstaller un paquet ?

- Pour supprimer un package en local, il faudra utiliser la commande :

> npm **uninstall express**

OR
> npm **un express**

- Pour supprimer les packages du cache, il faudra utiliser la commande : 
> npm cache clean