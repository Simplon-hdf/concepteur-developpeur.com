# Table des matières

- [Table des matières](#table-des-matières)
- [Le Versioning](#le-versioning)
  - [Qu'est ce que c'est ?](#quest-ce-que-cest-)
  - [À quoi ça sert ?](#à-quoi-ça-sert-)
  - [Comment ça se caractérise avec Git ?](#comment-ça-se-caractérise-avec-git-)
- [Résumé](#résumé)

# Le Versioning

## Qu'est ce que c'est ?

Le versioning (ou versionnage en français) est un concept qui consiste en un repertoriage des versions d'un projet, d'un logiciel, d'un document... enfin toutes sortes de ressources qui sont amenées à évoluer dans le temps.

Pour faire simple : on conserve des versions différentes d'une ressource à différentes fins.

Voilà simplement ce qu'est le versioning.

## À quoi ça sert ?

Le versioning est très utile pour différentes raisons.

Ne vous est-il jamais arrivé de retourner lire du code d'un projet que vous aviez fait il y a quelques années ?
Ne vous êtes vous jamais rendu compte que votre point de vue sur un sujet avait changé ?

Si la réponse à ces questions est "Oui", alors cette version de vous a evolué par rapport à celle d'il y a quelques années. Dans ce cas de figure, vous prennez conscience du chemin parcouru. Sans le savoir, vous avez déjà été confronté au versioning avant même de lire un quelconque article sur le sujet. Ça peut paraître abstrait pour le moment, prenons donc un exemple plus concret :

```
Imaginons que vous travailliez sur un ancien projet, et que vous deviez coder une fonction qui vous fait
encore faire des cauchemars tant son comportement était complexe. Il est plus que probable que
vous aimeriez avoir cette fonction pour pouvoir simplement la copier coller plutôt que de passer 
une semaine à faire des recherches et des tests infructueux, n'est ce pas ?
Vous allez dans la classe qui contient cette fameuse fonction mais vous vous souvenez que
vous l'aviez supprimé et avez arrêté ce projet. 
Vous n'avez aucun moyen de récupérer cette fonction et force est de constater que
vous allez devoir repasser par une étape de reflexion intense.
```

Si vous aviez utiliser un outil de versioning comme Git, vous auriez pu vous rendre à une version de cette classe, antérieure à la version dans laquelle la fonction a été supprimée.

Pour l'expliquer simplement :

Ne pas utiliser d'outil de versioning revient à travailler avec une seule version d'une application.
Utiliser un outil de versioning revient à créer une multitude de versions du code de votre application.

## Comment ça se caractérise avec Git ?

Le versioning est l'aspect principal de Git, tout tourne autour du concept de versioning avec Git, nous en parlerons un peu plus en détail dans l'[article](../../03-git-functions/fr/article.md) sur le fonctionnement de Git.

Les versions des fichiers d'un dépôt Git sont stockées dans un historique de "commit", avec Git on peut enregistrer des versions différentes de tout type de fichier quand on le souhaite. En reprenant l'exemple ci-dessus, nous pourrions imaginer qu'une fois que votre fonction était fonctionnelle vous ayez décidé de sauvegarder cette version de votre classe. Alors vous auriez pu récupérer votre fonction, même si elle n'existait plus dans la dernière version de votre code. Votre dépôt Git contient une version du fichier contenant cette fonction.

# Résumé

- Le versioning est un concept qui consiste en un repertoriage des versions d'une ressource.
- Un outil de versioning permet de sauvegarder les différentes versions d'une ressources à diverses fins.
- Git est logiciel qui se repose en grande partie sur le versioning, bien que ça ne soit pas le seul aspect qui le caractérise.
- Git permet de stocker différentes versions d'une ressource dans un historique par le biais d'un mécanisme appellé "commit".