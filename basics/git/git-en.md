# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Installation](#installation)
  - [Windows](#windows)
  - [Mac](#mac)
  - [Linux](#linux)
    - [Using APT](#using-apt)
    - [Using Pacman](#using-pacman)
- [Get Started](#get-started)
  - [Commands](#commands)
  - [Create empty repository](#create-empty-repository)
  - [Branches](#branches)
  - [Pull Request](#pull-request)
    - [How it works](#how-it-works)

# Introduction

Git is a software which was created in 2005 by Linus Torvalds (The Linux creator)

Git is a free soft, used to bring versionning of code and to permit to users to collaborate easyly on a project.

It make user to be able to share their code through a whole team (using some other platform/services) plus, Git do not need Internet connection to be used

# Installation

## Windows

To install Git under Windows, you can click [this link](https://git-scm.com/download/win)

## Mac

For Mac using `Homebrew`

```sh
brew install git
```

## Linux

For Linux it depends on your Linux Package Manager (based on your distribution)

### Using APT

```sh
sudo apt-get install git
```

### Using Pacman

```sh
sudo pacman -S git
```

# Get Started

This section will bring you some informations to get started with Git.

## Commands

| Commande                                  | Description                                                                                         |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------- |
| git init                                  | Will create a .git folder for git in the folder where it is executed                                |
| git config                                | Will permit you to modify current repository configuration                                          |
| git status                                | Displays the status of stage area, with each file which is staged ant each file which is not staged |
| git add <filename>                        | Will add the specified file to stage                                                                |
| git commit                                | Will send stage area content to local repository area                                               |
| git remote -add <alias> <remote_repo_uri> | Will bind your local repository to a remote repository                                              |
| git push <remote_alias>                   | Will send your local repository fresh content to remote repository                                  |
| git pull <remote_alias>                   | Will get the remote repository fresh content to your local repository                               |
| git fetch <remote_alias>                  | Will get any changes from the remote repository (like branches and commits)                         |
| git clone <remote_repo_uri>               | Will get a whole remote repository and send it into a created folder (named as remote repo)         |
| git branch <branch_name>                  | Create new branch                                                                                   |
| git checkout <branch_name>                | Will change working branch                                                                          |
| git merge <branch_to_merge>               | Will bring all commits from a branch to current branch                                              |

## Create empty repository

To create a new repository from scrath with Git you can proceed as follow : 

```sh
git init # Has to be executed in the folder you want to use a root for your project
git remote add <remote repository alias> <remote repository URI> # Conventionnaly alias is 'origin' for your remote repository
git add <files to stage> # This can be an folder name, multiples file names or '.' which is equal to 'all'
git commit -m "my commit message" # This is used to commit your staged changes, use quotes is recommended, and -m flag will permit you to specify directly the commit message but it's optionnal to use this flag
git push <remote repository alias> <branch_name> # Send local commited changes to remote repo
```

## Branches

## Pull Request

### How it works