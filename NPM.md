# Sommaire

- <a href='#whats-npm-fr'>Introduction a NPM</a>
- - <a href='#whats-npx-fr'>Introduction d'NPX</a>
- <a href='#whats-packages-fr'>Les paquets Node</a>
- <a href='#node-modules-fr'>Les modules Node</a>

# Qu'est ce que NPM (Node Package Manager) <a id='whats-npm-fr'></a>

NPM est un manager de paquet Node utilisé pour télécharger et publier des paquets Node avec les autres developpeurs qui utilisent NPM<br>
NPM se divisent en 3 grands axes :

1. Le site NPM

    Le site [NPM](https://www.npmjs.com/) sert à connaitre les paquets Node disponibles sur le Registry NPM.

2. CLI ou l'Interface en Ligne de Commande

    La CLI est une enorme partie du NPM puis-ce que c'est par le CLI que vous interragirez avec NPM et avec le Registry NPM afin<br> de télécharger des paquets s'y trouvant ou de publier vos paquets.

3. NPM Registry ou l'Enregisteur

    Le Registry NPM est enfaite une enorme base de donnée qui va contenir des applications prêtes à l'emploi,<br> ou simplement des paquets Node que vous pourrez télécharger afin de les utiliser ou les adapter à vos besoins pour les utiliser dans votre paquet.

## Qu'est ce qu'NPX (Node Package Executer) <a id='whats-npx-fr'></a>

Comme NPM est un gestionnaire de paquet Node, NPX est enfaite un executeur des paquets Node
grace à NPX il vous sera possible d'executer des paquets Node directement depuis le Registry de NPM.<br>
NPX vous permettra ainsi de ne pas avoir à télécharger au préalable le paquet Node pour l'executer<br>

<br>

# Node Package ou Paquet Node <a id='whats-packages-fr'></a>

Un package node est un fichier ou un dossier décrit par un fichier **package.json**.<br>
Le fichier **package.json** va donner des informations à propos de votre package, c'est pourquoi il faut que ce fichier contienne les informations les plus détaillées possible.<br>
Un package node peut être public ou bien privé [En savoir plus sur la visibilité des packages](https://docs.npmjs.com/about-private-packages), comme il peut être restreint à une certaine portée ou non [En savoir plus sur la portée des packages](https://docs.npmjs.com/about-scopes) 

Un package node peut être tout ce qui suit (Et bien plus encore) :

1. Un fichier ou un dossier décrit par un fichier **package.json**
2. Un fichier compressé contenant (1.)
3. Une URL pointant vers 2.
4. L'url d'un repos Github qui lorsque cloné donnera un fichier ou un dossier décrit par un fichier **package.json**

<br>

# Node Modules <a id='node-modules-fr'></a>

Un module Node est une dépendance dont votre paquet aura besoin pour s'executer ou simplement qui vous sera nécessaire pour le développement de votre package.<br>

Un module node peut être :

- Un dossier (Structuré comme un Package)
- Un fichier JS

Vous pouvez voir les module node dans le dossier ``` node_modules ```.<br>
Note : Il se peut qu'un module node ne se soit pas correctement installé, dans ce cas, il est conseillé de supprimer le dossier ``` node_modules ``` et de reinstaller tous les modules.<br>

Puis-ce qu'une image vaut mieux que mille mots :

![](https://guillaume-richard.fr/wp-content/uploads/2020/06/node-modules-app-performance.png)

<br>

Cette image explique à quel point les modules nodes sont une charge importante.<br>
Note : Il est très important de ne pas omettre le ``` node_modules ``` dans votre .gitignore afin de ne pas envoyer tous les modules sur votre dêpot distant.<br>