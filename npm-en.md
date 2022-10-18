# Summary

- <a href='#npm-introduction'>NPM Introduction</a>
- - <a href='#npx-introduction'>NPX Introduction</a>
- <a href='#node-packages'>Node Packages</a>
- <a href='#node-modules'>Node Modules</a>
- <a href='#package-json'>**package.json** file</a>
- <a href='#semantic-versioning'>Semantic Versioning</a>
- <a href='#diff-fields-dependencies'>Difference between ``` dependencies ``` and ``` devDependencies ```</a>
- <a href='#package-lock-json'>Introducing **package-lock.json**</a>
- <a href='#sources'>Sources</a>

# What's NPM (Node Package Manager) <a id='npm-introduction'></a>

NPM is a manager for Node Packages, used to publish packages and therefore share packages with other developpers using NPM.<br>
NPM is divided by 3 axes :

1. NPM Website
    
    The [NPM](https://www.npmjs.com/) website is an usefull resource to see which packages are availables on the NPM Registry.

2. CLI or Command Line Interface

    CLI's a very large part of NPM, because it's with CLI that you'll interact with NPM Registry.<br>
    You'll be able to download NPM packages from CLI, send yours, execute downloaded packages, so, it's a realy big part
    of NPM.

3. NPM Registry

    Registry is a huge database containing JS Packages, Registry can contain some JS applications or just some other packages.<br>
    That you'll be able to manage, adapt at your needs and so use in your own project.<br>
    But like it was said above, you can also get JS applications ready to use therefore, you can get applications and execute it.

## What's NPX (Node Package Executer) <a id='npx-introduction'></a>

Like NPM is a manager for packages, NPX is an executer for packages.<br>
It means you're able to execute packages contained on NPM Registry without downloading them.<br>
Note: You can also install packages with NPM and run them with NPM, but you'll need to download packages firstly.

# Node Packages <a id='node-packages'></a>

A Node Package is a file or directory described in a **package.json** file.<br>
The **package.json** file will give some information about package, that's why you have to add this **package.json** with the most detailled information.<br>
A Node Package can also be private or public [Read More About Package visibility](https://docs.npmjs.com/about-private-packages), and scoped or unscoped [Read More About Package scopes](https://docs.npmjs.com/about-scopes)

A node package can be all following (And more) : 

1. A folder containing program described by **package.json**
2. A compressed file like .tgz (1.)
3. A URL resolving to (2.)
4. An GitHub URL that when cloned, will give you a folder containing program described by **package.json**

# Node Modules <a id='node-modules'></a>

A Node Module is a dependency that your own package will need to run.<br>
It can be :

- An folder (Structured like an Package)
- An JS file

You can see Node Modules in ``` node_modules ``` folder.<br> 
Note: Sometimes a Node Module can be installed without some parts of, so you can delete ``` node_modules ``` folder to 
redownload cleanly Node Modules required by your package.<br>

A great resumed explanations of Node Modules could be : <br>

![](https://guillaume-richard.fr/wp-content/uploads/2020/06/node-modules-app-performance.png)

<br>

Because you're forced to download dependencies for each package, who'll need some other packages.

# **package.json** <a id='package-json'></a>

**package.json** as explained above is a file who'll be essential for your Node Package.<br>
This file can be compared to a map of your Package, you'll provide a lot of information in.<br>
You'll put in following information (Not exhaustive, and again more) :

- name : How is named your package
- version : Version of your package
- description : Put an description to your package
- keywords : Pretty optional but if you want to share your package with other developpers, it would be indispensable
- homepage : It can be a GitHub repos or a Website, just the web referer to your package
- bugs : Where to report bugs, can also be a repos git to issues page
- author : Some information about you
- main : Used as entry point of your Node Package / Module
- scripts : For advanced configuration of your package [Read More about script possibles values](https://docs.npmjs.com/cli/v8/using-npm/scripts)
- dependencies : To add a dependency to your project with targeted package name as key and version of targeted package as value ``` "express":"4.18.2" ``` will add dependency of express version 4.18.2 for example 
- devDependencies : To add a developpement depency on your package, see below
- private : true ; To be sure your package can't be published if you want to keep it private

And many others again. <br>

If you do not specify ``` scripts ``` for example, nmp will generate a default parameter, this way specifications aren't required if you do not need to do specifics things.<br>

# Semantic Versioning <a id='semantic-versioning'></a>

Semantic Versioning is a standard that you'll must use when you'll put significative modification update to your own package.<br>
It's recommended to publish your changes with a different package version, ``` version ``` field in your **package.json**.<br>
That way, other developers who depend on your code can understand the extent of changes in a specific version.<br>

There is something you need to know to approach the following, you will need to understand some terms:

1. MAJOR : MAJOR version when your update will break dependencies
2. MINOR : MINOR version when your update (Adding a feature for example) will be compatible with previous version
3. PATCH : PATCH version when your update make backwards compatibles bug fixes

You can also [take a look to semantic versioning specifications](https://semver.org/) to improve your knowledge on this.<br>

There is specifications for semantic versioning :

- It's recommended to start package versions at ``` 1.0.0 ```
- When you'll do a MAJOR update, you'll increase by 1 the first digit ``` 2.0.0 ``` like's named, it's a major update
- When you'll do a MINOR update, you'll increase by 1 the middle digit ``` 2.1.0 ``` like's named, it's a minor update
- When you'll do a PATCH update, you'll increase by 1 the last digit ``` 2.1.1 ```

To go deeper with semantic versioning using with NPM, you can consult this [Article](https://docs.npmjs.com/about-semantic-versioning#using-semantic-versioning-to-specify-update-types-your-package-can-accept) 

# Difference between Dependencies and devDependencies <a id='diff-fields-dependencies'></a>

Dependencies are some packages that you'll need to use to run your package.<br>
DevDependencies are some packages that you'll need to use to work on your package.<br>

For example, if you want to cook a cake and taste your cake :

For cooking, you'll be able to use a Beater or just an Fork.<br>
Where Beater is an devDependencies, usable but optional, you can also use a Fork as devDependencies.<br>
Fork can be used to eat your cake too, it could be a Dependency too.<br>

# **package-lock.json** <a id='package-lock-json'></a>

**package-lock.json** is an automaticly generated file, it will be generated on any operations where NPM modify ``` node_modules ``` tree or ``` package.json ```.<br>
**package-lock.json** contains an exact description of dependencies tree was generated. <br>
This file is intended to be commited to repository could be useful for :

- Describe a single representation of dependency tree, that way every aspects of continuous integration are guaranteed to install exactly the sames dependencies.
- Provide an easy way for user to retrace the states of ``` node_modules ```.
- Provide a greater visibility of tree changes.
- Optimize dependencies installation by allowing NPM to skip previously installed dependencies.

**package-lock.json** format :

- ``` name ``` : Will be same as field in ``` package.json ```
- ``` version ``` : Will be same as field in ``` package.json ```
- ``` lockfileVersion ``` : It's an integer version (Following same standart about semantic versions in ``` package.json ```)
[Read more about](https://docs.npmjs.com/cli/v8/configuring-npm/package-lock-json#lockfileversion) 

And more about, [here](https://docs.npmjs.com/cli/v8/configuring-npm/package-lock-json#packages)

# Sources <a id='sources'></a>

- [What's NPM](https://www.w3schools.com/whatis/whatis_npm.asp)
- [Introduction of NPX](https://www.geeksforgeeks.org/what-are-the-differences-between-npm-and-npx/)
- [Node Modules & Node packages](https://docs.npmjs.com/about-packages-and-modules)
- [**package.json** file](https://docs.npmjs.com/cli/v8/configuring-npm/package-json)
- [Semantic Versioning with Node](https://docs.npmjs.com/about-semantic-versioning)
- [Semantic Versioning](https://semver.org/)
- [Difference between ``` dependencies ``` and ``` devDependencies ```](https://stackoverflow.com/questions/18875674/whats-the-difference-between-dependencies-devdependencies-and-peerdependencies)
- [**package-lock.json** file explanations](https://docs.npmjs.com/cli/v8/configuring-npm/package-lock-json)