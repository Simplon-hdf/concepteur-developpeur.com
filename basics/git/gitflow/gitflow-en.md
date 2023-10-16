# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Installation](#installation)
  - [Windows](#windows)
  - [Mac](#mac)
  - [Linux](#linux)
    - [Apt](#apt)
    - [Pacman](#pacman)
- [Get Started](#get-started)
  - [Initialisation](#initialisation)
  - [Features Branches](#features-branches)
    - [Creation](#creation)
    - [Finalisation](#finalisation)
  - [Fixes Branches](#fixes-branches)
    - [Creation](#creation-1)
    - [Finalisation](#finalisation-1)

# Introduction

GitFlow is a **workflow** whose permitting to work on separated branches, in that way it will semantically be easy to identificate what changes are brang by branches.

Using GitFlow is an way to work optimally on a project, using specific branches for specific kind of changes.
It's telling to everyone by the nature of the branch, what kind of work has been achieved throught this branch.

Although the fact that GitFlow is just an method to work, a program exists to use Git automated for GitFlow way.

# Installation

## Windows

Under Windows, Git already contains GitFlow module, so, if you've already installed Git, you can use GitFlow module, otherwise, [install Git here](https://git-scm.com/download/win).

## Mac

To install GitFlow module under Mac using HomeBrew :

```sh
brew install git-flow
```

## Linux

### Apt

To install GitFlow module under Linux using Apt :

```sh
sudo apt-get install git-flow
```

### Pacman

To install GitFlow module under Linux using Pacman :

```sh
sudo pacman -S git-flow
```

# Get Started

## Initialisation

To initialise GitFlow, you have to execute the command :

```sh
git flow init
```

In a folder whose can already be a git repository, or no.

![git init](assets/gitflow-init.png)

It's recommended to name main branch as `main` instead of `master`.

For the rest, you can set the name that you want, although the default name are preferred to be keep in most cases.

## Features Branches

Features branches are useful when you have to start new feature development, although they're just basic branches, they bring semantical information about what changes are made throught those branches.

They indicate clearly to everybody that the changes made into them will concern a new feature development.

### Creation

### Finalisation

## Fixes Branches

### Creation

### Finalisation
