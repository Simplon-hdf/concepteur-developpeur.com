## Les linters 


<br/>


# Sommaire

- [Qu'est-ce qu'un linter](#whoisLinter)  
- [Linter VS. Débugger](#lintervsdebugger)  
- [Linters existants](#linterExistant)
  - [JSLint](#linterExistant)
  - [JSHint](#linterExistant)
  - [ESLint](#linterExistant)
  - [Comparaison des différents linters](#differenceBetween)
- [Exemple avec ESLint](#ESLint)
- [Incorporation dans le processus d'intégration continue](#IncorporationProccessIntegration)


<br/>


### Qu'est-ce qu'un linter ?  <a name="whoisLinter"></a>

Le linter est un outil automatisé d'analyse de code. Il analyse en temps réel notre code et prévient des erreurs, pour cela, il s'éxecute **avant** que le code ne soit compilé (ou exécuté - selon le langage utilisé). Le linter est donc un outil d'analyse **statique** du code. Il existe trois majeures façons d'utiliser un linter: En _ligne de commande_, dans une _extension_ de l'éditeur de code, ou dans le processus de _développement continu_. Cette dernière option permet à chaque commit d'être corrigé et formatté. 
Le linter est souvent utilisé en parralèle d'un **formatter** et d'autres outils. C'est un outil différent qui ne remplace pas le débuggeur. 

_exemple:_ 
> _Un script déstiné à tourner sur serveur ne doit pas contenir l'objet window. Il est possible de configurer le linter pour nous prévenir de cette erreur._ 

<br/>


### Différence avec un débugger <a name="lintervsdebugger"></a>

Le débuggeur peut également être considéré comme un outil de gestion des erreurs, cependant, c'est un outil **dynamique**! Le débuggeur permet donc de décomposer l'éxecution du code afin de détecter des erreurs dynamiques : type des variables, gestion de mémoire, ... 

<br/>


### Les linters existants  <a href="linterExistant"></a>

Il existe différents linter: 

* **JSLint** : JSLint est un linter livré prêt à l'emploi et simple à utiliser. Il ne nécessite que peu de configurations (pas de fichier de config) et ne permets pas la personnalisation de règles personnelles. Ses explications concernant les erreurs sont parfois obscures. 
* **JSHInt** : JSHint est un linter se plaçant entre JSLint et ESLint. S'il accepte un fichier de configurations, celles-ci restent limitées. La configuration de règles personnelles n'est pas disponible. Ce linter offre deux options d'utilisation, ce qui peut rendre son utilisation complexe. 
* **ESLint** est le plus connu et le plus utilisé. C'est un linter extrêmement flexible et configurable qui possède également en son sein un formatter. Il est possible de configurer des règles personnelles dans un fichier de configuration. Son installation et sa configuration complexe au premier abord peut rebutter le débutant. Il peut de plus s'intégrer au processus de développement continu.

<a href="differenceBetween"></a>

|        | Facilité d'utilisation | Configurable | Documentation | Clareté des explications | Extensible | Support ES6 / JSX |
|:------:|:----------------------:|:------------:|:-------------:|:------------------------:|:----------:|:-----------------:|
| JSLint |            ✔️           |       ❌      |       ❌       |             😐            |      ❌     |        ES6        |
| JSHint |            😐           |       😐      |       ✔️       |             😐            |      😐     |        ES6        |
| ESLint |            😐           |       ✔️      |       ✔️       |             ✔️            |      ✔️     |     ES6 + JSX     |

_Ces trois linters proposent une alternative de correction du code directement sur navigateur, nous ne recommandons pas cette pratique aux développeurs._ 

<br/>

<a name="#ESLint"/>

## Exemple avec ESLint

### Installation et configuration : Projet vs. Global

1) Créer un dossier projet, puis y adjoindre un environnement node. 
   > mkdir newProject  
    npm init -y

2.1) Installer ESlint en configuration par défaut
   > npm init @eslint/config  
   
2.2) **OU** Installer Eslint avec sa configuration Airbnb
   > npm i eslint eslint-config-airbnb-base eslint-plugin-import

note: Il est également possible d'installer ESlint en global avec cette commande (ajout du -g), mais cette installation est déconseillée par la documentation officielle Eslint :  
   > npm i eslint eslint-config-airbnb-base eslint-plugin-import -g

3) En l'absence de configuration officielle lors de l'installation d'EsLint, il est important de créer son fichier de configuration. 
   > touch .eslintrc  
     code .eslintrc

4) Dans le fichier de configuration, insérer la configuration suivante: 

   > {  
  "extends": ["airbnb-base"],  
  "env": {  
    "node": true,  
    "es6": true,  
    "browser": true  
  },  
  "rules": {  
    "no-console": "off"  
  }  
}  

5) Installer l'extension "Eslint" sur votre éditeur de code favori. Fermer puis relancer, votre Eslint est maintenant disponible! 

6) Il est également possible d'utiliser Eslint en ligne de commande directement depuis votre terminal: 
    Pour une installation **globale**: 
> eslint index.js  

    Pour une installation **locale**: 
> npx eslint index.js  

7) Il est à savoir qu'il existe de nombreux flags permettant de spécifier les actions à effectuer. La liste complète des flags est disponible avec cette commande. 
> npx eslint -h

<br/>

<a name="#IncorporationProccessIntegration"/>

### Incorporation dans le processus d'intégration continue: 


_ATTENTION: Ce tutoriel est écrit dans le cadre d'un projet Gitlab, Gitlab étant particulièrement permissif dans les outils Devops proposés._

<!-- Insert about Github actions -->

1) Sur Gitlab, ouvrir les **_settings_** de votre projet, puis aller dans **_CI/CD_**, puis **_runners_**
 > Vous devriez voir apparaitre deux colonnes: **Shared** runners et **Specific** runners

2) Les runners sont des machines virtuelles permettant d'executer une image de notre application sous **docker**. Le fichier de configuration _.gitlab-ci.yml_ permet de spécifier: 
   - Quelle image utiliser?
   - Quel script exécuter ? 
   - Quelles dépendances installer ? 

  > touch .gitlab-ci.yml

3) Remplir le fichier de configuration : 
  > image: node  
    stage:  
    \# I just want to lint, so I will create a "lint" stage  
    \- lint  
    \# Lets name our Job eslint, because that's what it's doing.  
    eslint:  
    \# tell eslint what stage it is. (This could also be build or test for example)
    stage: lint   
    \# What scripts do we want to run?  
    script:  
    # install eslint  
    - npm i eslint  
    # Run eslint  
    - node_modules/eslint/bin/eslint.js  

4) Commit et push le fichier. 

5) Pour voir le linter en action, aller dans **jobs**  

6) Pour aller plus loin: De nouveau, le fichier de configuration permet de configurer la convention choisie, il suffit dans le script de préciser les configurations souhaitées. Si il y en a plusieurs, séparer par le caractère "\\" (_backslah_)

  > script:   
    \# Install eslint   
    - |    
    npm install eslint \   
    eslint-config-airbnb \   
    eslint-config-prettier \   
    eslint-plugin-flowtype \ # Any ideas on what I might want to do next?   
    eslint-plugin-import \   
    eslint-plugin-jsx-a11y \   
    eslint-plugin-prettier \   
    eslint-plugin-react   

<br/>

_ _ _ 

sources: 
> https://medium.com/medvine/install-eslint-global-with-airbnb-style-guide-and-use-it-in-vscode-d752dfa40b    
  https://eslint.org/docs/latest/user-guide/getting-started   
  [1] https://runebook.dev/fr/docs/prettier/cli