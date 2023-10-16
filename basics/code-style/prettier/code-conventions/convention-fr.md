## Tables des matières

- [Définition](#définition)
- [Les conventions les plus couramment utilisées](#les-conventions-les-plus-couramment-utilisées)

# Définition 

Il existe plusieurs façons d'écrire un même code. De manière à uniformiser le code de différents développeurs dans les entreprises, des **conventions** existent. Ces conventions permettent aux développeurs d'uniformiser le code.

Les conventions couvrent différents domaines :

- Style d'indentation
- Type de déclaration des variables
- Agencement organisationnelle / structurelle (Qui concernent la façon de le projet sera agencé) 

Dans ce cadre, les **linters** et **formatteurs** permettent de "modifier" un code source afin de l'uniformiser de façon constante.

Suivre ces règles de convention apporte différents avantages : 

- Une meilleure maintenance logicielle (40 à 80 % de réduction du coût de maintenance)
- Améliore la lisibilité du code pour d'autres ingénieurs logiciel et rends plus facile la code review. 

# Les conventions les plus couramment utilisées 

Les plus grandes compagnies ont sorti leurs conventions respectives concernant Javascript :

- [**Standard Style Guide**](https://github.com/standard/standard) : Contient un linter et un formatter, suivi par Github, NPM, Heroku, MongoDB. De plus en plus utilisé dans l'OpenSource.
  - Pas de configuration, simple à utiliser et suivre.
  - Formatter automatiquement le code

- [**Google Style Guide**](https://google.github.io/styleguide/) : Google a sorti un guide pour Javascript, mais également pour HTML / CSS / C++ / TypeScript ou Angular. 
  - Pris en charge par ESLint. 

- [**Airbnb Style Guide**](https://github.com/airbnb/javascript) : Un des plus populaires. Très complet, des objets au testing. Propose des conventions CSS, JS, Ruby et React. Il est apprécié pour ça :
    - Consistence
    - lisibilité
    - Prédictibilité
    - Efficacité 

- [**Clean Code Style Guide**](https://github.com/ryanmcdermott/clean-code-javascript) : Tiré du livre de Robert C. Martin, les principes de ce livre ont été repris et appliqués au Javascript. C'est une liste de bonnes pratiques pour une écriture lisible du JavaScript.

**_Nous faisons le choix de suivre la convention proposée par AirBnb dans une stack JavaScript._**