# Table des matières

- [Table des matières](#table-des-matières)
- [Introduction](#introduction)
- [Linter != Débogueur / Débugueur (Debugger)](#linter--débogueur--débugueur-debugger)
- [Les linters les plus utilisés](#les-linters-les-plus-utilisés)
  - [JSLint](#jslint)
  - [JSHint](#jshint)
  - [ESLint](#eslint)
  - [Analyse comparatives](#analyse-comparatives)
- [ESLint en pratique](#eslint-en-pratique)
  - [Prise en main](#prise-en-main)
    - [Installation](#installation)
    - [Configuration](#configuration)

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

# ESLint en pratique

## Prise en main

### Installation

### Configuration