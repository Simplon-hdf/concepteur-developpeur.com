# Table des matières

- [Table des matières](#table-des-matières)
- [Introduction](#introduction)
- [Linter != Debbuger](#linter--debbuger)
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

# Linter != Debbuger

Le linter et le debbuger sont 2 programmes bien distincts, là où le linter s'occupe de gérer les erreurs du code en édition de ce dernier (pré-compilation / pré-transpilation), le debbuger intervient lors de l'étape de conversion du code source en code machine, le debbuger permet alors d'identifier certains type d'erreur dont le linter ne s'occupe pas.

De plus le debbuger permet de lire des informations sur certains processus, tel que la pile d'appel par exemple.

# Les linters les plus utilisés

## JSLint

## JSHint

## ESLint

## Analyse comparatives

# ESLint en pratique

## Prise en main

### Installation

### Configuration