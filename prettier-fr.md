# Sommaire

<!-- TOC -->
  * [Les formateurs](#les-formateurs)
    * [Qu'est-ce qu'un formater et pouquoi l'utiliser?](#quest-ce-qu--un-formater-et-pouquoi-lutiliser)
    * [Comment l'utiliser? L'exemple de Prettier](#comment-lutiliser-lexemple-de-prettier)
    * [Configurer Prettier :](#configurer-prettier-)
  * [Conclusion](#conclusion)
<!-- TOC -->

## Les formateurs

### Qu'est-ce qu'un formater et pouquoi l'utiliser? 

Toujours dans l'optique de suivre des conventions données, le **formateur** permet une retouche du code original afin que le code sortant corresponde à un style constant (défini au préalable). 

En d'autres termes, si le linter analyse statiquement l'_intérieur_ de notre code, le formater au contraire prends en charge l'_extérieur_, soit la partie visuelle.  

Utiliser donc le **formateur** pour votre style et le **linter** pour vos bugs ! 

Example: 

Une fonction peut être déclarée de la façon suivante: 
  > function init({ option1, option2, option3, option4, option5, option6, option7 }) {  
    //...   
    }   

Un formateur sortira le code source précédent en modifiant son aspect visuel, sa syntaxe (Indentation, Espace, etc)
  > funtion init ({   
      option1,   
      option2,    
      option3,   
      option4,   
      option5,   
      option6,   
      option7   
    })   

<br/>


### Comment l'utiliser? L'exemple de Prettier
 
**Prettier** peut être utilisé de différentes manières : 

1) La plus simple: L'extension VSCode. 

  - Installer l'extension VSCode "Prettier"
  - Utiliser la combinaison de touche "Ctrl + Shift + I"
  - Le fichier se formate automatiquement selon la configuration Prettier ! 

_Note: Il est possible dans les settings de configurer l'extension, ou de de créer un fichier de configuration._  


2) La _command line interface_:  


  - Installer prettier dans l'environnement node choisi ou de façon globale (ajout du _-g_ en fin de commande d'installation):
  A la racine du dossier projet: 
  > npm init -y
  > npm install --save-dev --save-exact prettier
  - Utiliser la commande pour formater le code, la sortie est formatée ! 
   Si installation globale:
  > prettier index.js
   Si installation locale / projet: 
  > npx prettier index.js

  - Autre option utile, si vous souhaitez que le formatage s'effectue directement dans le fichier, ajoutez _--write_ 
  > npx prettier index.js --write

  - Pour formater tous les fichiers du projet pris en compte par prettier, ne pas spécifier de fichier: 
  > npx prettier --write

  - Il est possible de créer un fichier _.prettierignore_ afin d'y spécifier les éléments qui ne doivent pas être formatés.

  - Le drapeau _--check_ en commande produit un message lisible par l'utilisateur afin d'informer de l'état des fichiers: 
  > npx prettier --ckeck 

  - Le drapeau _--debug-check_ permet d'activer un "débuggeur" pour le formatage du code, ce drapeau ne peut être utilisé avec _--write_. 

  - Le drapeau _--no-config_ permet d'utiliser la configuration Prettier par défaut.

  - De nombreux autres drapeaux sont disponibles en source ¹

<br/>

### Configurer Prettier : 

_Dans cet exemple, nous suivons la convention proposée par airbnb_

I) Installation globale et locale en CLI: 

De la même façon qu'il est possible de configurer ESLint de façon à suivre la convention Airbnb, il est possible de configurer Prettier au moyen du fichier _.prettierrc_

Dans le fichier _.prettierrc_ (s'il n'existe pas, créez le avec _touch .prettierrc_), coller: 
> {  
  "semi": false,  
  "tabWidth": 2,  
  "singleQuote": true  
  }  

II) Configurer l'extension VScode: 

- Cocher la case "Prettier : semi"
- Cocher la case "Single Quote"
- Dans "Prettier: Tab Width", renseigner la valeur 2.

- Il est également possible d'accéder au ficher global de configuration avec la commande : 
> code . /home/$USER/prettierrc.json
Puis de coller le code suivant: 
> {  
  "semi": false,  
  "tabWidth": 2,  
  "singleQuote": true  
  }  

<br/>

## Conclusion

Vous devriez maintenant être en mesure, selon votre type d'installation favori, d'installer l'outil souhaité et de le configurer selon la convention choisie par votre équipe! 
Dans ce tutoriel, nous avons volontairement occulté les formateurs disponibles dans les prettiers ! 
Sentez-vous libre de rechercher plus de documentation à ce sujet dans les différentes sources disponibles !

sources:  
  https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode  
  https://www.codereadability.com/automated-code-formating-with-prettier/  
  https://runebook.dev/fr/docs/prettier/cli (1)