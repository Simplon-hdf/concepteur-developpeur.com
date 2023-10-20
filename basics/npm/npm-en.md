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

That way other developpers using your package can follow what are change that you bring for each version.

To understand following, you must understand some terms :

1. MAJOR : We call MAJOR a version that's not backwards compatibles, which bring breaking changes.
2. MINOR : We call MINOR a version that's just bring some changes (like addition a new feature), but keep your package backwards compatibles.
3. PATCH : We call PATCH a version that's just bring bug fixes stuffs and keep backwards compatibles (Mostly often)

Tips : [Learn more about semantic versioning specifications](https://semver.org/)

There's some global specifications of semantic versionning :

- It's recommended to start your package developement to `1.0.0` version
- When you want to release PATCH changes, your package will pass to `1.0.1` version
- When you want to release MINOR changes, your package will pass to `1.1.0` version, as you can see, PATCH digit returned to 0
- When you want to release MAJOR changes, your package will pass to `2.0.0` version, as you can see, MINOR digit returned to 0

It's important to understand that when you release MAJOR version, that influences MINOR and PATCH.
When you release MINOR, that influcenses PATCH.

Note : Digits aren't limited to 9, a version `2.3.19` is completely correct.

You can [learn more](https://docs.npmjs.com/about-semantic-versioning#using-semantic-versioning-to-specify-update-types-your-package-can-accept)

# Differences between `dependencies` and `devDependencies`

The field `dependencies` allow you to list which dependencies that your package will need to run.
The field `devDependencies` allow you to list which dependencies that your package will need to work in development phase.

Ok let's take an example, imagine that you want to bake a cake :

To prepare your cake what do you'll **need** ?
Maybe a fork to beat eggs

Ok, but you can also take this fork to eat your cake.

In that example, that fork is a devDependency **AND** a dependency.

Because you'll need this fork to prepare it and to eat it.

# The package-lock.json file

The `package-lock.json` file is automaticaly generated by Npm when an operation on `node_modules` tree occurs.
The `package-lock.json` will contain a reliable description of evolution of `node_modules` tree.

This file is supposed to be included into repo, it can be useful to :

- Obtain only one version of `node_modules` tree and ensure continuous integrations principles.
- Obtain an easy way to retrieve `node_modules` states
- Obtain a better visibility on changes of dependencies tree
- Optimize dependencies installation, to do not redownload already installed dependencies.

[Learn more about **package-lock.json** format](https://docs.npmjs.com/cli/v8/configuring-npm/package-lock-json)

# Commands

There's many commands to interact with Npm, in the following section you'll find some of them.

## Initialize a Node Project

If you wish to initialize a Node project, you'll need to type this command :

```sh
npm init
```

This command has to be executed into the root folder for your project.

It will ask you some parameters and create `package.json` file.

## Installing dependencies (modules)

### Production dependencies

You'll certainly need to import dependencies in your project, to do that, use the command :

```sh
npm install <package_name>
```

Let's take an real example :

```sh
npm install express
```

Note : You can use `install` or just `i`, it's even.

This command will download Express library files into `node_module` folder (folder that will be automaticaly created if it doesn't exists yet).

### Development dependencies

If you wish to download dependencies only for development phase, you must know this flag :

```sh
npm install <package_name> --save-dev
```

Real example :

```sh
npm install winston --save-dev
```

This command will download `Winston` in your `node_module` and define it as `devDependencies` into your `package.json` file.

### Reinstalling dependencies

In case that you want to import Node project without `node_modules` or that you lose yours for some reason, vous could need to redownload all dependencies, for that case, you should know that command :

```sh
npm install
```

This command will read `dependencies` and `devDependencies` and download each packages.

# References