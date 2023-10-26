# Table des Matières

- [Table des Matières](#table-des-matières)
- [Travaillez en collaboration avec Git](#travaillez-en-collaboration-avec-git)
  - [L'enfer c'est les autres](#lenfer-cest-les-autres)
  - [Plateforme collaborative : GitHub](#plateforme-collaborative--github)
  - [Un workflow (Flux de travail)](#un-workflow-flux-de-travail)
  - [Le dépôt distant](#le-dépôt-distant)
- [Conclusion](#conclusion)
- [Résumé](#résumé)

# Travaillez en collaboration avec Git

## L'enfer c'est les autres

Git sert en grande partie à partager du code avec d'autres développeurs, et donc travaillez avec ces derniers sur un projet. Nous verrons dans cet article, les différentes contraintes que cela implique mais aussi les avantages que cela représente. 

## Plateforme collaborative : GitHub

Une plateforme largement reconnue dans le monde du développement est GitHub. Elle est de loin la plateforme la plus populaire et les développeurs du monde entier l'utilisent pour héberger leurs projets. Bien qu'il existe d'autres plateformes du même genre, telles que GitLab ou BitBucket, GitHub est la préférée des développeurs. C'est pourquoi nous avons decidé de la présenter ici.

GitHub est une plateforme qui héberge tous un tas de dépôt Git. Et permet, en plus de collaborer avec d'autres développeurs, de sauvegarder un dépôt Git de façon distante (sur le cloud), ce qui représente un avantage majeur : La décentralisation de projets. Imaginons que vous veniez à perdre toutes les données de votre disque dur, tous vos projets seraient perdus. Sauf si vous les aviez décentralisés grâce à GitHub. Dans ce cas, vous pourriez récupérer votre projet depuis un autre ordinateur.

En plus d'être sécurisante pour votre progression, GitHub est très ergonomique et facile à utiliser. Bien qu'elle puisse paraître abrupte pour un néophyte, l'essayer c'est l'adopter. Nous consacrerons un chapitre complet à GitHub tant il y a de chose à en dire.

## Un workflow (Flux de travail)

Un workflow est une façon de travailler, il existe différent type de façon de travailler en collaboratioo avec Git et les dépôts distants, cela peut-être vu comme des conventions ayant pour objectif de fluidifier le travail collaboratif. Ces conventions existent pour réduire le temps passé à manipuler les outils collaboratifs.

Nous aborderons ce sujet bien plus tard, cette section est à but introductif et il s'agit d'un sujet bien trop vaste pour être aborder ici.

## Le dépôt distant

S'il existe des dépôt locaux, il en existe aussi des distants. Ce qu'on appelle "dépôt distant" sont simplement des dépôts locaux qui ont étés envoyés sur des plateformes en ligne (telle que Git). Il y une distinction très claire à faire entre ces deux types de dépôt :

- Un dépôt local est un dépôt stocké sur votre machine.
- Un dépôt distant est un dépôt stocké sur un serveur en ligne.

La nuance peut sembler évidente, cependant, il y quelques subtilités qu'il est bon de connaitre afin de bien démarrer avec GitHub.

Un dépôt distant est une version qui peut être différente de votre version local de ce dépôt, il existe des commandes afin de récupérer la dernière version du dépôt distant, nous les verrons un peu plus tard. Dans le cas où vous travaillez avec d'autre personne, il est nécessaire que vous preniez conscience que votre version du projet est peut-être obsolète, vous serez donc souvent amenés à manipuler ces commandes.

# Conclusion

Cette introduction au travail collaboratif avec Git et GitHub est terminé, nous aborderons ces aspects plus en profondeur dans la prochaine section.

# Résumé

- Travailler en collaboration présentes de nombreux avantages mais représente aussi certaines contraintes.
- Il existe des façon de travailler sur un projet en collaboration afin de fluidifier cette dernière, c'est ce qu'on appelle un "workflow" (flux de travail).
- Il existe des plateformes permettant de décentraliser un projet Git.
- GitHub est la plateforme préférée des développeurs.
- Envoyer un dépôt local sur une de ces plateformes crée une nouvelle version de ce dépôt sur les serveurs de la plateforme.
- Il existe des commandes Git spécialement dédiées à la gestion des dépôts distants.