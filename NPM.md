# Les commandes NPM

# Comment initialiser un projet avec NPM ?

> **npm init**

Le npm init va créer un fichier **package.json** qui va permettre d'obtenir des informations sur son projet.

### Comment installer des modules ?

- ##### Pour pouvoir ajouter un nouveau pacquet à son projet il faudra utiliser :

**Exemple :**

> **npm install express**
OR 
> **npm i express**

 

- ##### Pour pouvoir installer les pacquet déjà existants il faudra utiliser :

> **npm install**
OR
**npm i**

Cette commande va permettre d'installer tous les pacquet et modules qui ont été ajoutées au projet dans le fichier **package.json**.

- ##### Vous pouvez télécharger une version spécifique d'un package pour revenir à une version antérieur, il vous faudra donc utiliser :

**Exemple :**

> **npm install express@1.0.2**


### Comment installer les pacquet de dépendance de développement ?

- ##### Pour installer les outils qui ne seront utilisés que dans l’environnement de développement, il faudra utiliser :

##### Exemple : 

> **npm install nodemon --save-dev**

Il y aura donc dans le fichier **package.json** le **devDepencies** qui va être ajouter.