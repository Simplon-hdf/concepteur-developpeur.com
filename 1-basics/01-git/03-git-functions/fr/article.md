# Table des Matières

- [Table des Matières](#table-des-matières)
- [Fonctionnement de Git](#fonctionnement-de-git)
  - [Terminologie de Git](#terminologie-de-git)
    - [Le Commit](#le-commit)
  - [À quoi ça sert exactement ?](#à-quoi-ça-sert-exactement-)
  - [Comment on s'en sert exactement ?](#comment-on-sen-sert-exactement-)
- [Résumé](#résumé)

# Fonctionnement de Git

## Terminologie de Git

Avant d'aborder le fonctionnement interne de Git, il est nécessaire que vous connaissiez un peu les termes de Git ainsi que les différents mécanismes et concepts qui le régisse.

### Le Commit

Un commit est un point dans l'évolution d'un fichier. Prenons une image pour expliquer cette phrase :

![commits schem](../assets/commits.png)

Comme vous pouvez le voir sur ce schéma, les commits sont stockés au sein d'un historique, cet historique permet de tracker l'évolution des fichiers de votre dépôt local (nous aborderons ce terme juste après). Le terme "commit" pourrait se traduire comme validation dans ce contexte. En fait, un commit est effectué de façon manuel par l'utilisateur de Git, nous allons prendre un exemple :

Vous avez développé une fonction qui vous a torturé l'esprit et la dernière chose que vous voulez est d'avoir à la réécrire parce que vous l'auriez perdu ou supprimer sans possibilité de la récupérer. Dans ce cas vous allez interagir avec Git et effectuer un "commit" pour que cette fonction soit gravée dans le marbre et que même si vous veniez à supprimer cette fonction par inadvertence, elle continuerait d'exister quelque part dans une version antérieure de votre fichier (stockée dans votre dépôt local).

En demandant à Git de faire un "commit" (d'effectuer une validation), vous avez en fait dit à Git de créer une nouvelle version de votre fichier. Version dans laquelle votre fonction existe quoi qu'il advienne de votre fichier de code (à une seule exception dont nous parlerons dans la section dédiée au dépôt).

Un commit est donc une validation de modification, à laquelle s'ajoute quelques options. En fait, pour effectuer un commit il y a un impératif, donner un "nom" à ce commit. Enfin on parle de message, ce message va servir à décrire ce que fait votre commit. Si nous reprenons l'exemple du dessus, un message de commit correct serait quelque chose du genre : "Implémentation de ma super fonction très utile". En attribuant un message à votre commit c'est comme si vous annotiez votre modification. De la même manière que vous écrivez des commentaires de code. Sachez qu'un message de commit est obligatoire.

Notez d'ailleurs que plus votre message de commit est descriptif, plus vous vous remercierai lorsque vous chercherez une modification bien particulière et que vous la trouverez gràce à la clareté de vos messages.

Maintenant que nous avons parlé du message du commit, nous allons parler de la façon dont vous allez dire à Git quel fichier vous voulez inclure dans votre commit. Et pour cette partie, nous allons avoir besoin d'un bon vieux schéma :

![commits scope schem](../assets/commits-scope.png)

Les commits peuvent affecter 1 fichier ou un ensemble de fichier. Par exemple (et c'est très généralement recommandé) vous pourriez vouloir qu'un commit affecte un seul et unique fichier, pour des raisons d'atomicité. Si c'est le cas, prennez un cookie et ne changez rien, c'est ce qu'il faut. Mais parfois, vous avez des modifications qu'il serait illogique de scinder dans des commits différents. Dans ce cas, vous pouvez très bien dire à Git de créer 1 commit pour 2 fichiers.

En réalité, qu'un commit affecte un ensemble de fichier n'est pas dramatique du tout, il faut simplement que ça vous parraisse logique de le faire de cette façon, et surtout le plus important, que ça ne devienne pas une contrainte dans le futur. Ce n'est pas le genre de chose qui peuvent être expliqué, seule votre expérience avec Git vous le fera comprendre. Mais sachez qu'une fois que vous aurez compris (en pratique) comment fonctionnent les commits et à quoi ils servent, vous ne pourrez plus vous passer de Git.

Mais étant donné que vous lisez cet article pour en apprendre plus sur Git et plus précisement cette section pour en apprendre plus sur les commits, nous allons quand même essayer de comprendre pourquoi ceux qui ont pris un cookie en ont eu le droit.

Bien imaginons simplement que :

```
Vous travaillez sur un projet avec Git et vous faites des modifications
mais des commits un peu moins, vous effectuez beaucoup de modifications
tant et si bien qu'au bout d'un moment.. votre programme ne fonctionne plus
du tout. Alors vous en chercher la cause en mettant les mains dans le code.
Mais pas moyen de mettre la main sur la ou les modifications responsables.
Et evidemment, votre dernier commit remonte à il y a deux heures.
Vous n'avez pas d'autre choix que de vous torturez l'esprit et passer en
revue tout ce que vous avez fait depuis deux heures. Ou restaurer la version
de votre code qui supprime toutes les modifications que vous avez effectué
depuis ces deux heures. Vous êtes dans une situation certes peu enviable
mais bien mérité, c'est en faisant des erreurs que l'on apprend, vous n'êtes
pas prêt d'oublier cette leçon et vous résignez à avoir perdu deux heures
de votre vie.
```

## À quoi ça sert exactement ?

## Comment on s'en sert exactement ?

# Résumé