# Table des Matières

- [Table des Matières](#table-des-matières)
- [Les commandes Git](#les-commandes-git)
  - [Initialiser Git dans un projet](#initialiser-git-dans-un-projet)
  - [Préparer des modifications à un commit](#préparer-des-modifications-à-un-commit)
  - [Enregister un commit](#enregister-un-commit)
  - [Conclusion](#conclusion)
  - [Résumé](#résumé)

# Les commandes Git

Les commandes Git sont la façon d'interagir avec Git. Elles permettent de dire à Git d'effectuer telle ou telle action. Ces commandes sont entrées dans votre terminal (shell). Cet article présente les commandes les plus basiques. Si vous n'avez pas lu l`[article](../../03-git-functions/fr/article.md) sur le fonctionnement de Git, veuillez en prendre connaissance avant de lire celui-ci.

## Initialiser Git dans un projet

Pour initialiser Git dans un projet, entrez la commande suivante :

```sh
git init
```

Cette commande aura pour effet de créer un dossier `.git` dans le répertoire dans lequel vous vous trouvez au moment de son exécution. Par exemple si vous etiez dans `/mon_projet_git/`, alors un dossier `.git` aura été crée dans ce dossier et vous y accèderiez en vous rendant à `/mon_projet_git/.git`. Il est possible que vous ne voyez pas de dossier `.git`, le `.` avant `git` en fait un dossier caché, tapez la commande `ls -al` et vous devriez le voir apparaître.

Voilà, Git est initialisé dans votre projet.

## Préparer des modifications à un commit

Pour préparer les fichiers qui ont subi des modifications, entrez la commande suivante :

```sh
git add [nom_du_fichier]
```

Ce qui aura pour effet de mettre votre fichier dans la stage area.

```sh
git add index.js
```

Mettra index.js dans la stage area et vous pourrez alors inclure ce fichier à votre prochain commit.

Notez qu'il possible de faire la même opération sur un dossier complet :

```sh
git add mon_dossier/
```

Ce qui aura pour effet de mettre tous les fichiers ayant subi des modifications de ce dossier dans la stage area.

Il est aussi possible, mais relativement délicat que vous souhaitez ajouter tous vos fichiers dans un commit, dans ce cas :

```sh
git add .
```

Qui aura pour effet de déplacer tous les fichiers ayant reçu des modifications dans la stage area, à partir du repertoire dans lequel vous exécutez cette commande. Par exemple, si vous utilisez cette commande dans : `/mon_projet_git/articles/` alors tous les fichiers contenus dans `/mon_projet_git/articles/` ainsi que tous ceux dans les dossiers de ce dossier. De façon récursive.

Évitez au maximum cette approche, sauf si vous ne modifiez qu'un fichier à la fois et que vous faites vos commits en temps réel.

## Enregister un commit

## Conclusion

## Résumé