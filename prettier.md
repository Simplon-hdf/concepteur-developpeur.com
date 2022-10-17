## Les formatteurs

### Qu'est-ce qu'un formatter et pouquoi l'utiliser? 

Toujours dans l'optique de suivre des conventions données, le **formatteur** permet une retouche du code original afin que le code sortant correspond à un style consistent. 

En d'autres termes, si le linter analyse statiquement l'_intérieur_ de notre code, le formatter au contraire prends en charge l'_extérieur_, soit la partie visuelle.  

Utiliser donc le **formatteur** pour votre style et le **linter** pour vos bugs! 

Example: 

Une fonction peut être déclarée de la façon suivante: 
  > function init({ option1, option2, option3, option4, option5, option6, option7 }) {  
    //...   
    }   

Un formatter sortira le code source donné en modifiant son aspect visuel, son style: indentation, espaces, ...
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

  - Commencer par installer l'extension VSCode "Prettier"
  - Utiliser la combinaison de touche "Ctrl + Shift + I"
  - Votre fichier se formatte automatiquement selon la configuration Prettier! 

_Note: Il est possible dans les settings de configurer l'extension, ou de de créer un fichier de configuration._  


2) La _command line interface_:  


  - Commencer par installer prettier dans l'environnement node choisi OU globalement (ajout du _-g_ en fin de commande d'installation):
  A la racine du dossier projet: 
  > npm init -y
  > npm install --save-dev --save-exact prettier
  - Utiliser la commande pour formatter le code, l'output sort formatté! 
   Si installation globale:
  > prettier index.js
   Si installation locale/projet: 
  > npx prettier index.js

  - Autre option utile, si vous souhaitez que le formattage s'effectue directement dans le fichier, ajouter _--write_ 
  > npx prettier index.js --write

  - Pour formatter tous les fichiers du projet pris en charge par prettier, ne pas spécifier de fichier: 
  > npx prettier --write

  - Il est possible de créer un fichier _.prettierignore_ afin d'y spécifier les éléments qui ne doivent pas être formattés.

  - Le drapeau _--check_ en commande produit un message lisible par l'utilisateur afin d'informer de l'état des fichiers: 
  > npx prettier --ckeck 

  - Le drapeau _--debug-check_ permet d'activer un "débuggeur" pour le formattage du code, ce drapeau ne peut être utilisé avec _--write_. 

  - Le drapeau _--no-config_ permet d'utiliser la configuration Prettier par défaut.

  - De nombreux autres drapeaux sont disponibles en source [1]

<br/>

### Configurer Prettier : 

_Dans cet exemple, nous suivons la convention proposée par airbnb_

I) Installation globale et locale en CLI: 

De la même façon qu'il est possible de configurer ESLint de façon à suivre la convention Airbnb, il est possible de configurer Prettier au moyen du fichier _.prettierrc_

Dans le fichier _.prettierrc_ (si non existant, le créer avec _touch .prettierrc_), coller: 
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

Vous devriez maintenant être en capacité, selon votre type d'installation favori, d'installer l'outil souhaité et de le configurer selon la convention choisie par votre équipe! 
Dans ce tutoriel, nous avons volontairement occulté les formatteurs disponibles dans les prettier! Sentez-vous libre de rechercher plus de documentation à ce sujet dans les différentes sources disponibles!

sources:  
  https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode  
  https://www.codereadability.com/automated-code-formatting-with-prettier/  
  [1] https://runebook.dev/fr/docs/prettier/cli