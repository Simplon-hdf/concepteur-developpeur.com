# Table des matières

- [Table des matières](#table-des-matières)
- [Introduction](#introduction)
- [Linter != Débogueur / Débugueur (Debugger)](#linter--débogueur--débugueur-debugger)
- [Les linters les plus utilisés](#les-linters-les-plus-utilisés)
  - [JSLint](#jslint)
  - [JSHint](#jshint)
  - [ESLint](#eslint)
  - [Analyse comparatives](#analyse-comparatives)
- [Prise en main d'ESLint](#prise-en-main-deslint)
  - [Initialisation](#initialisation)

# Introduction

Un linter est un programme qui analyse en **temps réel** le code écrit par un développeur, de sortes à notifier le développeur des potentielles erreurs qui pourrait se produire, comme l'appelle à une fonction qui n'existe pas par exemple.

Le linter peut intervenir dans divers contexte tels que :

- Au sein de l'éditeur de code
- Dans un processus de developpement partagé (Tels que sur GitHub par exemple)
- Être exécuté dans un terminal de façon manuelle, ou automatique avant la transpilation du code source

# Linter != Débogueur / Débugueur (Debugger) 

Le linter et le debugger sont 2 programmes bien distincts, là où le linter s'occupe de gérer les erreurs du code en édition de ce dernier (pré-compilation / pré-transpilation), le debugger intervient lors de l'étape de conversion du code source en code machine, le debugger permet alors d'identifier certains type d'erreur dont le linter ne s'occupe pas.

De plus le debugger permet de lire des informations sur certains processus, tel que la pile d'appel par exemple.

# Les linters les plus utilisés

## JSLint

JSLint est un linter livré prêt à l'emploi et simple à utiliser. 
Il ne nécessite pas de configuration mais en contre partie il ne permet pas de définir des critères concernant les erreurs. 
Ses explications concernant les erreurs sont parfois obscures.

## JSHint

JSHint est un linter livré prêt à l'emploi et simple à utiliser. 
Il ne nécessite pas de configuration mais en contre partie il ne permet pas de définir des critères concernant les erreurs. 
Ses explications concernant les erreurs sont parfois obscures.

## ESLint

**ESLint** est un linter extrêmement flexible et configurable qui peut faire office de formatter. 
Il est possible de configurer des règles concernant les erreurs dans un fichier de configuration.

## Analyse comparatives

📕 : Non<br/>
📙 : Partiellement<br/>
📗 : Oui<br/>
󠀠
| Linter | Facilité d'utilisation󠀠󠀠 󠀠󠀠󠀠󠀠󠀠󠀠󠀠 | Configurable󠀠 | Documentation󠀠 | Clareté des explications󠀠 | Extensible 󠀠 | 󠀠Support ES6 / JSX |
| ------ | ----------------------- | ------------ | ------------- | ------------------------ | ----------- | ------------------ |
| JSLint | 📗                   󠀠    | 📕            | 📕             | 📙                        | 📕           | ES6    󠀠            |
| JSHint | 📙                       | 📙            | 📗             | 📙                        | 📙           | ES6                |
| ESLint | 📙                       | 📗            | 📗             | 📗                        | 📗           | ES6 + JSX          |

# Prise en main d'ESLint

## Initialisation

Pour initialiser ESLint il vous faut un projet Node.

Puis vous devez exécuter la commande suivante dans la racine de votre projet Node :

```sh
npm init @eslint/config
```

Ce qui aura pour effet de vous demandez si vous voulez installer le module ESLint, si vous ne l'avez pas déjà.

Puis vous aurez une liste de paramètre à définir, si vous avez envie, il existe une alternative plus courte qui consiste à exécuter une installation préfaite :

```sh
npm install eslint eslint-config-airbnb-base eslint-plugin-import
```

Puis vous pouvez créer le fichier de configuration d'ESLint `.eslintrc.json` et y insérez le code suivant :

```json
{  
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
```

Ce qui aura pour effet de configurer ESLint avec la convention Airbnb de base.

Voila, ESLint est initialisé pour votre projet et vous notifiera des erreurs de code.