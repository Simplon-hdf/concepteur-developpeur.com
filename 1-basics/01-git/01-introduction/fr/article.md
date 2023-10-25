# Table des Matières

- [Table des Matières](#table-des-matières)
- [Introduction à Git](#introduction-à-git)
- [Un brin d'histoire](#un-brin-dhistoire)
- [Quelles utilités](#quelles-utilités)
- [Résumé](#résumé)

# Introduction à Git

Cet article est dédié à présenter le logiciel Git, vous trouverez ici des informations utiles sur ce qu'est Git et vous apprendrez son histoire.

# Un brin d'histoire

Git est un logiciel gratuit inventé par Linus Torvalds en 2005 et qui est distribué sous la license GNU2. Ce qui en fait un logiciel libre.

# Quelles utilités

Git est un logiciel absolument essentiel pour tout développeur, vous en comprendrez les raisons en lisant cette section.

L'idée première de Git est de pouvoir suivre l'évolution des modifications qu'à reçu un fichier, qu'il contienne du code ou non d'ailleurs. C'est dans cette optique que Git a été crée en plus de permettre de partager ces fichiers avec d'autres développeurs.

Prenons un exemple concret pour vous aider à comprendre ce à quoi Git sert :

```
Vous travaillez sur un projet en JavaScript,
et que vous fassiez des modifications dans votre code.
Puis vous vous rendez-compte que les modifications que
vous avez effectué créent un bug dans votre projet.
Malheureusement, vous devez chercher la cause du bug
et supprimer tout ce que vous avez fait depuis deux heures.
```

Il est plus que probable que vous vous soyiez déjà retrouvé dans cette situation. Git rend ce genre de chose très facile à gérer.

Nous allons prendre à nouveau cet exemple mais en utilisant Git pour vous aider à comprendre son utilité.

```
Vous travaillez sur un projet en JavaScript,
et à chaque modification significative de votre code
vous faites un "commit" (on verra ce terme plus tard).
Vos modifications créent un bug dans votre projet.
Git vous permet de cibler les modifications, vous pouvez
alors comparer directement les versions de votre code et
retirer uniquement la modification qui pose souci.
```

Quand vous utilisez Git en faisant un "commit", c'est comme si vous preniez une photo de votre code, à la différence qu'avec Git, vous pouvez revenir à un point antérieur dans le temps.

Voilà pour ce à quoi sert Git, nous y reviendrons dans le prochain [article](../../02-versioning/fr/article.md).

# Résumé

- Git est un logiciel libre et gratuit crée par Linus Torvalds en 2005.
- Git sert à avoir plusieurs versions d'un même fichier.
- Git permet de partager du code (mais pas que) entre les développeurs.
- Git est mandatory pour les développeurs.