# Table des matières

- [Table des matières](#table-des-matières)
- [La gestion de projet selon le Manifeste Agile](#la-gestion-de-projet-selon-le-manifeste-agile)
- [Les 4 valeurs de la méthode agile](#les-4-valeurs-de-la-méthode-agile)
  - [Les principes de la méthode agile ](#les-principes-de-la-méthode-agile-)
  - [Les fondamentaux de la méthode agile. ](#les-fondamentaux-de-la-méthode-agile-)
    - [Productivité](#productivité)
    - [Communication client](#communication-client)
    - [Communication](#communication)
- [SCRUM (La mêlée)](#scrum-la-mêlée)
  - [Les roles](#les-roles)
    - [Product Owner](#product-owner)
    - [Scrum Master](#scrum-master)
    - [L'équipe de développement](#léquipe-de-développement)
  - [Le Product Backlog](#le-product-backlog)
  - [Le Sprint backlog](#le-sprint-backlog)
  - [Les rituels / cérémonies](#les-rituels--cérémonies)
    - [Le sprint planning](#le-sprint-planning)
    - [Le daily meeting](#le-daily-meeting)
    - [La sprint Review](#la-sprint-review)
    - [La sprint Retrospective](#la-sprint-retrospective)


# La gestion de projet selon le Manifeste Agile

La gestion d'un projet suivant le manisfeste Agile place le client au centre du cycle de vie de ce dernier, en incluant le client au proccessus de mise en place du projet, l'équipe Agile peut ajuster le développement du projet en fonction de l'évolution du besoin du client dans le temps.

La méthode Agile se compose de 4 valeurs et de 12 principes.

# Les 4 valeurs de la méthode agile

- **L'équipe**

Des individus et des interactions, plutôt que des processus et des outils.

- **L’application**

Des fonctionnalités opérationnelles plutôt que de la documentation exhaustive.

- **La collaboration**

Une collaboration avec les clients plus qu'une négociation contractuelle.

- **L’acceptation du changement**

Il est préferable d'accepter le changement et de ne pas suivre de plan rigide.

## Les principes de la méthode agile <a name="pma"></a>

- Satisfaire le client avec un produit de qualité et répondant au besoin
- Accueillir les demandes de changements
- Mise à jour fonctionnelle fréquente 
- Collaboration quotidienne au sein de l'équipe
- Créer un lien de confiance
- Communication face à face
- Prioriser la continuité face à la nouveauté
- Faire avancer le projet avec un rythme constant
- Rigueur technique et conception avancée qui renforce l’agilité
- Minimiser le superflu pour se concentrer sur l’essentiel
- Auto-responsabilité des membres de l’équipe
- Adaptation des comportements et du travail dans l’équipe régulièrement après les rituels

## Les fondamentaux de la méthode agile. <a name="fma"></a>

### Productivité

- Fournir fréquement des solutions fonctionnelles.
- Prioriser les solutions importantes.
- Segmenter la production du projet.
- Une ligne de conduite rigoureuse lors du développement du projet.
- Productivité constante.
- La simplicité et l'art de maximisé la quantité de travail qu’on ne fait pas.

### Communication client

- Le client fait partie de l'équipe.
- Communication permanante avec le client.
- Établir une relation de confiance avec le client.

### Communication 

- Adaptation et amélioration de l'équipe.
- Privilégier le contact humain.
- Le contact humain facilite la compréhension des différentes contraintes de chaque partie prenantes.
- Communication verbal et non verbal (communication face à face).
- Auto-responsabilisé les membres de l'équipe.

# SCRUM (La mêlée)

SCRUM est un **framework** (cadre de travail) permettant de mettre en place la methodologie Agile de façon incrémentale et itérative.

![Scrum](assets/scrum_schema.jpeg)

## Les roles

### Product Owner

Le Product Owner (PO) est un membre névralgique sur lequel repose une charge de travail très importante, en effet, il se charge de la communication entre le client et l'équipe, il organise le Product Backlog en fonction des tâches à prioriser et régit globalement le cycle de vie du projet.

### Scrum Master

Le SCRUM master a pour rôle de s'assurer que le framework SCRUM est bien mis en application, il est aussi responsable de l'animation des rituels Agile.

### L'équipe de développement

L'équipe de développement est composée de developpeur qui auront à leur charges de développer les fonctionnalités du projet.

## Le Product Backlog

Le product backlog est un registre dans lequel l'équipe pioche des tâches à réaliser.

Le PB est rempli par le Product Owner et peut contenir :

- Des **user-stories** : Les user-stories sont des tâches simples expliquant une fonctionnalité du produit, les user-stories peuvent se décomposer en sous-tâche qui serviront d'étapes à l'accomplissement de la user-story liée. Les user-stories sont formattées comme suit "En tant que .. je peux .. afin de .." ou "En tant que .. je dois .. afin de ..", voici un exemple concret : "En tant qu'apprenant je dois m'identifier afin de participer à ma promotion". De cette façon les développeurs savent ce qu'ils doivent faire pour cette fonctionnalité, l'user-story répond à : `Qui ? Quoi ? Pourquoi ?` Il ne restent plus qu'au développeur de répondre au `Comment ?`.

- Des **Epics** : Les Epics sont un ensemble d'user-stories, en générale, les Epics représentent une fonctionnalités complète là où les user-stories représentes des fragment de fonctionnalités. Une Epic pourrait être `Identification des utilisateurs` et pourrait contenir l'user-story dans l'exemple de user-story.

![Product Backlog](assets/backlog.png)

## Le Sprint backlog

Le **Sprint backlog** est un registre contenant des tâches à effectuer pour livrer une fonctionnalité, une fois qu'un sprint est terminé l'équipe, se réunie afin pour les rituels agiles retrospéctif afin d'identifier différents axes d'amélioration et définie les nouvelles tâches pour le prochain sprint.

Dans le framework Scrum, on distingue deux types de **backlogs** :

- Le **registre de produit** (ou product backlog)
- Le **sprint backlog** (registre d'itération)

![](https://bubbleplan.net/blog/wp-content/uploads/2018/05/430.jpeg)

## Les rituels / cérémonies

### Le sprint planning

Le sprint planning est un rituel SCRUM qui réunit le Product Owner et l'équipe de développement afin de plannifier le Sprint à venir, ensemble ils établissent une liste de tâche à mettre dans le Sprint Backlog en se basant sur la priorité des tâches ou en fonction de la dernière itération, à la fin du sprint planning, l'équipe de développement sait quelles tâches devront être réalisées lors du prochain sprint.

### Le daily meeting

Le daily meeting est un rituel dont la charge revient à l'équipe de développement et comme son nom l'indique, il a lieu tout les jours, en générale avant de commencer à travailler sur le projet (vous pourrez aussi entendre parler de Stand Up Meeting).
Ce rituel ne doit pas dépasser 15 minutes dans un soucis d'efficacité.
Lors de ce rituel les membres de l'équipe doivent répondre aux questions :

- Qu'est ce que j'ai fais hier ?
- Quels obstacles ai-je rencontré ?
- Qu'est ce que je vais faire aujourd'hui ?

Si une problématique notable est relevée, elle doit faire l'objet d'une réunion ultérieure afin d'être résolue.

### La sprint Review

La sprint Review est le seul rituel qui incluent les parties prenantes du projet, ce rituel réunit :

- Le client
- Le SCRUM Master
- Le Product Owner
- L'équipe de développement

Il faut compter 1 heure par tranche d'1 semaine de sprint, c'est à dire que si un sprint a une durée de 2 semaines, la review durera 2 heures.

Ce rituel sert à l'équipe de présenter l'état d'avancement du projet à toutes les parties prenantes, de cette façon, le client peut faire part de ses impressions quant au projet, ou dire que le projet nécéssite quelques ajustements.

Avec ce rituel, toutes les parties prenantes s'assurent que le projet avance dans la bonne direction.

De plus, il peut arriver qu'à l'issue d'un sprint, le product owner annule ce rituel pour certaines raisons, nottament lorsque le sprint à rencontré des difficultés à être achevé et n'est donc pas présentable.

### La sprint Retrospective