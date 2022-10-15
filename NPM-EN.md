# Summary

- <a href='#npm-introduction'>NPM Introduction</a>
- - <a href='#npx-introduction'>NPX Introduction</a>
- <a href='#node-packages'>Node Packages</a>
- <a href='#node-modules'>Node Modules</a>
- <a href='#package-json'>**package.json** file</a>

# What's NPM (Node Package Manager) <a id='npm-introduction'></a>

NPM is an manager for Node Packages, used to publish packages and therefore share packages with other developpers using NPM<br>
NPM is divided by 3 axes.

1. NPM Website
    
    The [NPM](https://www.npmjs.com/) website is a usefull resource to see which packages are availables on the NPM Registry

2. CLI or Command Line Interface

    CLI's a very large part of NPM, because it's with CLI that you'll interact with NPM Registry.<br>
    You're able to download NPM packages from CLI, send yours, execute downloaded packages, so, it's a realy big part
    of NPM.

3. NPM Registry

    Registry is a huge database containing JS Packages, Registry can contain some JS applications or just some other packages
    That you'll be able to manage, adapt at your needs and so use in your own project.<br>
    But like it was said above, you can also get JS applications ready to use therefore, you can get applications and execute it

## What's NPX (Node Package Executer) <a id='npx-introduction'></a>

Like NPM is an manager for packages, NPX is an executer for packages.<br>
It means you're able to execute packages contained on NPM Registry without downloading them<br>
Note: You can also install packages with NPM and run them with NPM, but you'll need to download packages firstly

<br>

# Node Packages <a id='node-packages'></a>

An Node Package is a file or directory described in a **package.json** file
The **package.json** file will give some informations about package, that's why you have to add this **package.json** with the most detailled informations.<br>
A Node Package can also be private or public [Read More About Package visibility](https://docs.npmjs.com/about-private-packages), and scoped or unscoped [Read More About Package scopes](https://docs.npmjs.com/about-scopes)

A node package can be all of following (And more) : 

1. A folder containing program described by **package.json**
2. An compressed file like .tgz (1.)
3. An URL resolving to (2.)
4. An GitHub URL that when cloned, will give you an folder containing program described by **package.json**

<br>

# Node Modules <a id='node-modules'></a>

A Node Module is an dependency that your own package will need to run
It can be :

- An folder (Structured like an Package)
- An JS file

You can see Node Modules in ``` node_modules ``` folder<br>
Note: Sometimes an Node Module can be installed without some parts of, so you can delete ``` node_modules ``` folder to 
redownload cleanly Node Modules required by your package.<br>

An great resumed explanations of Node Modules could be : <br>

![](https://guillaume-richard.fr/wp-content/uploads/2020/06/node-modules-app-performance.png)

<br>

Because you're forced to download dependencies for each packages, who'll need some other packages.

# **package.json** <a id='package-json'></a>

**package.json** as explained above is a file who'll be essential for your Node Package.<br>
This file can be compared to a map of your Package, you'll provides a lot of informations in.<br>
You'll put in followings informations (Not exhaustive, and again more) :

- name : How is called your package
- version : Version of current package
- description : Put an description to your package
- keywords : Pretty optionnal but if you want to share package with other developpers, it would be indispensable
- homepage : It can be a github repos or a Website, just the web referer to your package
- bugs : Where to report bugs, also can be a repos git to issues page
- author : Some information about you
- main : Used to entry point of your Node Package / Module
- scripts : For advanced configuration of your package [Read More about script possibles values](https://docs.npmjs.com/cli/v8/using-npm/scripts)
- dependencies : To add a dependency at your project with version as value ``` "express":"4.18.2" ``` will add depency of express version 4.18.2 for example 
- devDependencies : To add a developpement depency on your package, see below
- private : true ; To be sure your package can't be published if you want to keep it private

And many others again. <br>

If you do not specify ``` scripts ``` for example, nmp will generate a default parameter, this way specifications arent required if you do not need to do specifics things.<br>