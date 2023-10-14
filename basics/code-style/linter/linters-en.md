# Summary

- [What is a linter](#whatisaLinter)  
  - [Linters difference table](#differenceBetween)  
- [Difference between Linter & Debugger](#lintervsdebugger)  
- [Existing linters](#existinglinters)
  - [JSLint](#existinglinters)
  - [JSHint](#existinglinters)
  - [ESLint](#existinglinters)
  - [Comparaison des différents linters](#differenceBetween)
- [Example with ESLint](#ESLint)
  - [Installation & Configuration](#Installandconfig)
- [Incorporation dans le processus d'intégration continue](#IncorporationProccessIntegration)
- [Sources](#Sources)

## Linters

### What is a linter? <a name="whatisaLinter"></a>

A linter is an automatic tool for code analysis. It analyses in live our code and warns us about errors. It runs **before** the compilation (or execution - according to your language). In this context, the linter is considered as a static tool.
Linter is often used with a **formatter** and other tools.
It exists three main ways of using a linter: With _command line interface_, in an _extension_ of your code editor, or in the process of _continuous integration_. This last option coupled to the formatter can automatically correct and format every new commit. 

It's not the same as the debugger and it can't replace it. 

_example :_
> _A servor-side script can't use the window object. It is possibl to configure the linter to prevent this kind of error._

### Difference between Linter and Debugger

The Debugger can also be considered as an error management tool, but it's **dynamic**! Debugger allows us to decompose the execution of our code and it helps us to detect dynamics errors: variable type, memory gestion, ...

### Existing linters

Today, there are different linter: 

* **JSLint**: JSLint is a linter that is delivered ready to use and simple to use. It requires little configuration (no config file) and does not allow customization of personal rules. Its explanations about errors are sometimes obscure. 
* **JSHint**: JSHint is a linter between JSLint and ESLint. If it accepts a configuration file, it is limited. Personal rule configuration is not available. This linter offers two usage options, which can make its use complex. 
* **ESLint**: The most used and most known. It's a very versatile and configurable linter. It also contain a formatter. It can be integrated in your _continuous integration_

_These three linters also allows us to correct our code directly in our browsers, but we don't recommand this practic._

<a href="differenceBetween"></a>

|        | Ease of use | Configurable | Documentation | Clarity of explanations | Extensible | Support ES6 / JSX |
|:------:|:----------------------:|:------------:|:-------------:|:------------------------:|:----------:|:-----------------:|
| JSLint |            ✔️           |       ❌      |       ❌       |             😐            |      ❌     |        ES6        |
| JSHint |            😐           |       😐      |       ✔️       |             😐            |      😐     |        ES6        |
| ESLint |            😐           |       ✔️      |       ✔️       |             ✔️            |      ✔️     |     ES6 + JSX     |

_These three linters offer an alternative to correct the code directly on the browser, we do not recommend this practice to developers._ 

### Example with ESLint

#### Installation & Configuration

1) Create a directory for your project and configure your node environment. 
   > mkdir newProject   
     npm init -y

2) Install ESLint and the Airbnb configuration
   > npm i eslint eslint-config-airbnb-base eslint-plugin-import

note: It is also possible to proceed to a global installation of ESlint (add -g), but this installation is not recommanded by the ESLint official documentation: 
   > npm i eslint eslint-config-airbnb-base eslint-plugin-import -g

3) We haven't config yet our ESLint. Let's create our config file: 
   > touch .eslintrc   
     code .eslintrc

4) In the config file _.eslintrc_, insert the following script: 
   >  {  
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

5) Now that you have ESLint installed and configured, install the "ESLint" extension. Close and restart, your ESLint is now available! 

6) ESLint can also be used with CLI (_command line interface_): 
    With a global config: 
   > eslint index.js

    With a local config: 
   > npx eslint index.js

_ _ _ 

sources: 
> https://medium.com/medvine/install-eslint-global-with-airbnb-style-guide-and-use-it-in-vscode-d752dfa40b    
  https://eslint.org/docs/latest/user-guide/getting-started   
  [1] https://runebook.dev/fr/docs/prettier/cli