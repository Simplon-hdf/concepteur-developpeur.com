# Table des Matières

- [Table des Matières](#table-des-matières)
- [Les commandes Git](#les-commandes-git)
  - [Initialiser Git dans un projet](#initialiser-git-dans-un-projet)
  - [Prépaer des modifications à un commit](#prépaer-des-modifications-à-un-commit)
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

## Prépaer des modifications à un commit

## Enregister un commit

## Conclusion

## Résumé