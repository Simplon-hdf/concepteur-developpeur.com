# Sommaire

- [What is a linter](#whatisaLinter)  
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
