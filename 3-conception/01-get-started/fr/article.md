# Table des Matières

- [Table des Matières](#table-des-matières)
- [Introduction](#introduction)
- [Bénéfices](#bénéfices)
- [Méthodes](#méthodes)
  - [Conception de fonctionnalité](#conception-de-fonctionnalité)
    - [Pseudo Code](#pseudo-code)
  - [UML (Unified Modeling Language)](#uml-unified-modeling-language)
- [Résumé](#résumé)

# Introduction

La conception d'application est un sujet très vaste. Elle regroupe divers aspects ou étapes qui surviennent avant la réalisation fonctionnelle du projet. La conception ne prends pas qu'une forme, elle se décline en une multitude de réalisation qui permettent de mettre en lumière les différents aspects d'un projet.

# Bénéfices

La conception permet aux membres d'une équipe de développement de décrire le comportement d'une application avant de commencer à développer, ce qui est très intéressant pour plusieurs raisons :

- Définir un comportement en ayant une vue d'ensemble sur la réalisation à produire
- Avoir une vision claire sur chacun des aspects de la réalisation
- Présenter les différents aspects de l'application à toutes les parties prenantes du projet
  - Obtenir des retours sur la conception afin de s'assurer que les fonctionnalités sont celles attendues par les parties prenantes
- Permettre une transmission des spécifications de l'application à chaque nouveau membre de l'équipe de développement

Voilà pour les bénéfices de concevoir un projet avant de le réaliser, notez d'ailleurs qu'il ne s'agit là que de bénéfices de groupe, mais la conception permet aussi d'aborder le développement d'un projet de façon complétement différente. Et de se poser les bonnes questions avant même de commencer à réaliser le projet, ce qui sur le long terme peut faire économiser énormément de temps et des efforts.

En concevant une application, vous deviendrez un bien meilleur développeur.

# Méthodes

Il existe plusieurs façons de concevoir une application ou une fonctionnalité, vous en découvrirez quelques-unes dans cette section.

## Conception de fonctionnalité

Il y a plusieurs façons de concevoir des fonctionnalités, une d'entre elle est l'**algorigramme** couplé au **pseudo-code**.
Cette méthode de conception est généralement utilisée pour les **développeurs** débutants, elle permet d'inculquer une logique algorithmique aux **développeurs**, en plus de permettre un découpage clair d'une fonctionnalité.

Notez que cette méthode n'est vraiment pas répandue à grande échelle car elle est relativement chronophage et assez rudimentaire, nous la présentons ici par acquit de conscience, mais si vous estimez avoir une bonne logique algorithmique, cette section ne sera pas la plus pertinente pour vous. Bien que vous devriez prendre connaissance de cette section afin de vous en assurer.

<img src="./../assets/algo-demo.png" style="width:50%;height:50%"/>

Voilà ce qu'est un algorigramme, il s'agit seulement d'une représentation schématique d'un algorithme.

Dans l'exemple ci-dessus, les carrés représente des actions. Les ronds ont une valeur sémantique pour dénoter le début et la fin d'un algorigramme. Les triangles quant à eux servent à représenter des conditions.

Un code couleur a été ajouté afin de séparer les actions, notez qu'en général, un algorigramme est utilisé pour représenter les actions du système. Ici, les actions dénotées en vert sont les actions utilisateur, alors que celles en rouge sont celles du système.

### Pseudo Code

Le pseudo code est un code qui n'en pas écrit dans un langage de programmation, mais dans une langue humaine. En français par exemple.

Note : Préferez rédiger vos ressources en Anglais afin d'être sûr de pouvoir rejoindre des équipes internationnales (Comme écrire vos commentaire de code en anglais par exemple).

En fait, le pseudo code peut être vu comme une représentation textuel d'un algorigramme, en voici un exemple en reprenant le précédent algorigramme :

```pseudo-code
Début de la procédure;
L'utilisateur sélectionne un article;
L'utilisateur ajoute son article au panier;
Si le nombre d'article dans le panier >= 1 :
  L'utilisateur valide le panier;
  L'utilisateur entre ses informations bancaire (Bank_ASK);
  L'utilisateur valide ses informations bancaire;
  Si les informations bancaires sont correctes :
    Si le solde du compte correspondant aux informations bancaires entrées par l'utilisateur est >= au prix du panier:
      Le système envoie un mail de confirmation à l'adresse mail associé au compte de l'utilisateur;
      Le système enregistre la commande de l'utilisateur.
    Sinon:
      Le système affiche un message d'erreur;
      Retourner à Bank_ASK;  
  Sinon: 
    Le système affiche un message d'erreur;
    Retourner à Bank_ASK;  
Sinon :
  Fin de la procédure.
Fin de la procédure.
```

Vous voudrez sans doute un exemple plus verbeux :

![](../assets/pseudo-code.png)

*<p style="text-align:center;">À gauche, le pseudo-code et à droite le code en langage de programmation.</p>*

Note: Les conditions auraient pu être inversé afin de ne pas créer autant de niveau d'imbrication, il s'agissait seulement de suivre l'algorigramme à la lettre afin de démontrer les 2 approches aussi fidèlement, en général, évitez au maximum plus de 2 niveaux d'imbrication.

## UML (Unified Modeling Language)

**UML est un LANGAGE**, bien que cela puisse sembler contre-intuitif, UML est bel et bien un langage.

UML est un langage qui permet de modéliser schématiquement les différents aspects d'une application ou d'un système par le biais de divers types diagrammes.

Nous en parlerons plus tard dans l'article : [Les bases d'UML](not-available.md)

# Résumé