# Table des Matières

- [Table des Matières](#table-des-matières)
- [Les branches](#les-branches)
  - [Ce que sont les branches](#ce-que-sont-les-branches)

# Les branches

Les branches sont un mécanisme qui permet de dupliquer l'historique de commits en plusieurs versions. Elles sont très utile dans des travaux collaboratifs. Leur utilisation de base est de séparer les modifications d'un développeur A de celles d'un développeur B. De cette façon, les développeurs ne se marchent pas dessus lors de leur travail.

Ce n'est pas la seule utilité des branches, nous verrons quelques utilisations tierces des branches dans un prochain article.

## Ce que sont les branches

Nous allons reprendre un schéma afin de visualiser :

![one branch](../assets/one-branch-repo.png)

Voilà à quoi votre dépôt ressemble, dans les faits, vous utilisez déjà une branche, nommée "main" qui signifie "principale". Donc vous effectuez vos modifications sur une branche nommée "main", vous avez donc un unique historique.

Voyons voir ce qu'il se passe si nous créeions une nouvelle branche :

![two branches](../assets/two-branch-repo.png)

Nous avons dupliqué l'historique de commit, ce qui fait qu'il en existe maintenant deux, c'est très utile pour permettre aux développeur de développer tranquillement. Voyons ce qu'il se passe si nous travaillons sur cette nouvelle branche.

![](../assets/new-commits.png)

Deux commits ont étés ajoutés à l'historique de la nouvelle branche, l'utilité de faire ça peu paraître abstraite, vous saisirez pleinement l'utilité des branches lorsque nous aborderons les travaux collaboritif avec Git.