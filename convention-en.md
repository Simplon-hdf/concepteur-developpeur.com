# Code conventions

## For what usage ? 

It exists differents ways of writing code. In a way to uniform code between developpers, companies began to develop some conventions. This conventions are used by teams for making their code intelligible and readable for all. 

Conventions covered differents domains: 

- Indentation style
- Conventions on how to name and how to structure your project's files.
- Commentaries and documentation of the source code
- Variable declaration

In this context, **linters** and **formatters** both tries to modify our source code in order to make it clean. 

Following this rules of convention gives lots of advantages like:

- A better software maintenance (40 to 80 % less cost of maintenance)
- Improve readabilty of code for other software engineers and make the process of _peer review_ easier.

## The different conventions : 

The biggest tech compagnies developss their own conventions for Javascript writing: 

* **Standard Style Guide** : Contains a linter and a formatter, follow by Github, NPM, Heroku or MongoDB.
    - No configuration, easy to use. 
    - Automatically format your code.
        >https://github.com/standard/standard_

* **Google Style Guide** : Google also released a guide for javascript, but also for HTML / CSS / C++ / TypeScript or Angular. 
    - Used by Default in ESLint
    > https://google.github.io/styleguide/

* **Airbnb StyleGuide** : One of the most popular. From objects to performance testing. Offer conventions for CSS, JS, Ruby and React. It is appreciated for it :
    - Consistency
    - Readability
    - Predictability
    - Efficacity
    > https://github.com/airbnb/javascript

* **Clean Code Style Guide** : Taken from the book of Robert C. Martin, principles of this book have been taken and applied to JavaScript development. It is more like a list of good practices for a better readability of Javascript. 
    > https://github.com/ryanmcdermott/clean-code-javascript


 **_In this tutorial, we will follow the Airbnb Convention with a JavaScript stack._**
