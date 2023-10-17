# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Linter != Debugger](#linter--debugger)
- [Most popular Linters](#most-popular-linters)
  - [JSLint](#jslint)
  - [JSHint](#jshint)
  - [ESLint](#eslint)
  - [Benchmark](#benchmark)
- [Get started with ESLint](#get-started-with-eslint)
  - [Initialisation](#initialisation)

# Introduction

A linter is a program which anaylize in **real time** code written by a developper, to prevent of potentials error can occured, as call to non existing function for example.

Linters can be configured to work in some context as following :

- In the code editor
- In a shared code process (As in GitHub for example)
- In a terminal manually triggered by a command, or automatically before transpilation 

# Linter != Debugger

Linter and Debugger are 2 distincts programs, linter will manage errors during edidion (before transpilation or compilation), the debbuger will manage errors during compilation / transpilation process, it will permit to identificate other kind of errors whose are ignored by linter.

Debbuger can provide more detailed informations on errors and bring some process obsvervation, like call stack for example.

# Most popular Linters

## JSLint

JSLint is a ready to use linter, right after installation. 
It do not requires configuration, but therefore, it do not allow you to define personnalized rules.
Error logging can be kinda weird.

## JSHint

JSHint is a ready to use linter, right after installation. 
It do not requires configuration, but therefore, it do not allow you to define personnalized rules.
Error logging can be kinda weird.

## ESLint

ESLint is a highly configurable linter which can be used as a formatter too.
It provide configuration of errors triggers rules in a configuration file.

## Benchmark

📕 : No<br/>
📙 : Partially<br/>
📗 : Yes<br/>
󠀠
| Linter | Ease of use 󠀠󠀠󠀠󠀠󠀠󠀠󠀠 | Configurability | Documentation󠀠 | Extensibility 󠀠 | 󠀠Support ES6 / JSX |
| ------ | ------------ | --------------- | ------------- | -------------- | ------------------ ||
| JSLint | 📗                   󠀠 | 📕               | 📕             | 📕           | ES6    󠀠            |
| JSHint | 📙                    | 📙               | 📗             | 📙           | ES6                |
| ESLint | 📙                    | 📗               | 📗             | 📗           | ES6 + JSX          |

# Get started with ESLint

## Initialisation

To initialize ESLint, you need a Node project.

You have to run following command into the project root :

```sh
npm init @eslint/config
```

NPM will ask you if you want to install ESLint if it didn't installed yet.

You'd see a list of parameters to set, set them and ESLint will create your personnal configuration based on parameters you's set.

A shorter way exists to install a pre made configuration :

```sh
npm install eslint eslint-config-airbnb-base eslint-plugin-import
```

Now, create a file named `.eslintrc.json` to the project root and insert this code :

```json
{  
"extends": ["airbnb-base"],  
"env": {  
  "node": true,  
  "es6": true,  
  "browser": true  
  },  
"rules": {  
  "no-console": "off"  
  }  
}  
```

There you go, ESLint is now configured with Airbnb convention for your project.