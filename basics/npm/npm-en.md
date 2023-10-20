# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [What is Npm (Node Package Manager)](#what-is-npm-node-package-manager)
- [What is Npx (Node Package Executer)](#what-is-npx-node-package-executer)
- [Node Packages](#node-packages)
- [Node Modules](#node-modules)
- [The package.json file](#the-packagejson-file)
- [Semantic Versioning](#semantic-versioning)
- [Differences between `dependencies` and `devDependencies`](#differences-between-dependencies-and-devdependencies)
- [The package-lock.json file](#the-package-lockjson-file)
- [Commands](#commands)
  - [Initialize a Node Project](#initialize-a-node-project)
  - [Installing dependencies (modules)](#installing-dependencies-modules)
    - [Production dependencies](#production-dependencies)
    - [Development dependencies](#development-dependencies)
    - [Reinstalling dependencies](#reinstalling-dependencies)
- [References](#references)

# What is Npm (Node Package Manager)

Npm is a **node package manager** used to import or publish Node packages with other developpers who uses Npm.

Npm is divided in 3 majors parts :

1. **Npm Website**

    The [Npm](https://www.npmjs.com/) website is useful to know which Node packages are availables on the Registry.

2. **CLI (Command Line Interface)**

    The CLI's the biggest part of Npm, because it's by the CLI that you'll **interact with Npm** and with the registry to **import packages** or **publish your packages**.

3. **Npm Registry**

    The **Npm registry** is a kind of a huge **database** who store **complete functionals application** and mostly **node packages** that you'll can **download** to use or **adapt** them to your needs.

# What is Npx (Node Package Executer)

Npx is a **Node package executer** (...).
Npx allow you to run remote packages, that means you didn' have to **download** them to **run**, you can just run package remotely by your **CLI** from the **registry**, it can be useful to run **complete functionals application**.

Please note that generally, we prefer perform remote run on light applications.

# Node Packages

A Node package si a file or a folder described by a file named **package.json** (Most often a folder)

The **package.json** file will provides several informations about your package, that's why you must fill it carefully with detailed informations.

A Node package can be public or private, [Read more about package visibilty](https://docs.npmjs.com/about-private-packages), it can also be restrained to a particulous scope. [Read more about packages scopes](https://docs.npmjs.com/about-scopes)

A Node package can be all following (And even more) :

1. A file or a folder described by a **package.json** file
2. A compressed file containing (1.)
3. An URL pointing to (2.)
4. An URL of GitHub repository that when cloned result to something formed as (1.)

# Node Modules

Node modules are dependencies that your package may have to need to run, or just used for development cycle of your package/application.

A Node Module can be :

- A folder
- A `.js` file

You can see modules in `node_modules` folder.

Note : A node module can be incompletely download for some reason, in that case, it's recommended to remove `node_modules` folder and reinstall packages by using [this command](#reinstalling-dependencies)

As an image's worth than thousand words : 

![](https://guillaume-richard.fr/wp-content/uploads/2020/06/node-modules-app-performance.png)

This image explains how heavy are Node modules.

Note : It hardly recommended to do not forget omitting `node_modules` folder in your `.gitignore` to do not push them in your remote repository.

# The package.json file

As explained above, the **package.json** file is essential to your Node package.

This file is like a map to your package, you'll provide 
many informations in this file.

```json
- "name" : Your package name
- "version" : Your package version
- "description" : The package description
- "keywords" : This field can be omitted, but it may be useful for peoples whose searching for your package, if you wish to publish it. 
- "homepage" : Can be a GitHub repository URL or just Website URL, it's represent the reference page of your package
- "bugs" : This field provide informations on where users have to go to ask for bugs fixes
- "author" : Some informations about you
- "main" : Will be used to run your package, it refers to your application entry point
- "scripts" : Allow an advanced configuration, [learn more](https://docs.npmjs.com/cli/v8/using-npm/scripts)
- "dependencies" : This field allow you to indicate Npm, which packages are needed to run yours.
- "devDependencies" : This field allow you to indicate Npm, which packages are useful / required for development phase
- "private" : This champ is used to ensure that your package is private or no (It's a boolean)
```

Npm will set default values to skiped fields, for instance, for the `script` field, Npm will set a test default value for this field.

# Semantic Versioning

Semantic Versioning is a standard that you should follow when you release significant modifications to your packages.

It's recommended to publish your changes with different versions, changing `version` field in your `package.json` file.

# Differences between `dependencies` and `devDependencies`

# The package-lock.json file

# Commands

## Initialize a Node Project

## Installing dependencies (modules)

### Production dependencies

### Development dependencies

### Reinstalling dependencies

# References