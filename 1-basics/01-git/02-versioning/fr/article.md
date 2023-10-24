# Table des matières

- [Table des matières](#table-des-matières)
- [Le Versioning](#le-versioning)
  - [Qu'est ce que c'est ?](#quest-ce-que-cest-)
  - [À quoi ça sert ?](#à-quoi-ça-sert-)
  - [Comment ça se caractérise avec Git ?](#comment-ça-se-caractérise-avec-git-)
- [Résumé](#résumé)

# Le Versioning

## Qu'est ce que c'est ?

Le versioning (ou versionnage en français) est un concept selon lequel, on répertorit les versions d'un ouvrage, un logiciel, un document... enfin toutes sortes de chose qui sont amenées à évoluer dans le temps.

Pour faire simple : on conserve des versions différentes d'une ressource à différentes fins.

Voilà simplement ce qu'est le versioning.

## À quoi ça sert ?

Le versioning est très utile pour différentes raisons.

Ne vous est-il jamais arrivé de retourner lire du code d'un projet que vous avez fait il y a quelques années ?
Ou ne vous êtes vous jamais rendu compte que votre point de vu sur un sujet avez changé ?

En fait, vous avez eu à faire au versioning bien avant de lire un quelconque article sur le sujet. Dans la première question, si la réponse est "Oui", alors on peut dire que la version de vous aujourd'hui est bien meilleure que celle d'il y a plusieurs années. Dans ce cas de figure, vous prennez conscience du chemin parcouru. Ça peut parraitre un peu abstrait pour le monent, prennons donc un exemple plus concret :

```
Imaginons que vous travallez sur un projet sur lequel vous avez travaillé
il y quelques années, et que vous deviez coder une fonction qui vous fait
encore faire des cauchemars tant son comportement été complexe. Il est
plus que probable que vous aimeriez avoir cette fonction pour pouvoir
simplement la copier coller plutôt que de passer une semaine à faire
des recherches et des tests infructueux, n'est ce pas ?
Vous allez dans la classe qui contient cette fameuse fonction mais
vous vous souvenez que vous l'aviez supprimé et avez arrêté ce
projet. Vous n'avez aucun moyen de récupérer cette fonction et
force est de constater que vous allez devoir repasser par une
reflexion intense.
```

Si vous aviez utiliser un outil de versioning comme Git, vous auriez pu vous rendre à une version de cette classe antérieure à la version dans laquelle la fonction à été supprimée.

Pour l'expliquer simplement :

Ne pas utiliser d'outil de versioning revient à travailler avec une seule version d'une application.
Utiliser un outil de versioning revient à créer une multitude de versions du code de votre application.

## Comment ça se caractérise avec Git ?

Avec Git, le versioning est l'aspect principal du logiciel, en fait, tout tourne autour du concept de versioning avec Git, nous en parlerons un peu plus en détail dans l'[article](../../03-how-it-works) sur le fonctionnement de git.

Les versions des fichiers d'un dépôt Git sont stockées dans un historique de "commit", avec Git on peut enregistrer des versions différentes de tout type de fichier quand on le souhaite, si on reprends l'exemple ci-dessus, on pourrait imaginer qu'une fois que votre fonction était fonctionnelle vous ayez décidé de sauvegarder cette version de votre classe. Et alors vous auriez pu récupérer votre fonction puis-ce que même si elle n'existait plus dans la dernière version de votre code, il y aurait eu une version de votre classe contenant votre fonction dans l'historique de "commit" de votre dépôt Git.

# Résumé

- Le versioning est un concept selon lequel il existe plusieurs versions d'une ressource.
- Un outil de versioning permet de sauvegarder les différentes versions d'une ressources à diverses fins.
- Git est logiciel qui se repose en grande partie sur le versioning, bien que ça ne soit pas le seul aspect qui le caractérise.
- Git permet de stocker différentes versions d'une ressource dans un historique par le biais d'un mécanisme appellé "commit".