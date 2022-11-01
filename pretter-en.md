# Sommaire

- <a href='#formatters'>Formatters</a>
    - <a href='#wawuf'>What's are and Why use formatters</a>
    - <a href='#how-use'>How use, Prettier Example</a>
    - <a href='#config-prettier'>How to configure Prettier</a>
- <a href='#conclusion'>Conclusion</a>
    - <a href='#sources'>Sources</a>

## Formatters

## What's are and why use Formatters <a id='wawuf'></a>

**Formatter** is a useful tool for following code conventions, with formatter you'll be able to modify your code to match with chosed code convention.<br>
That way, your code'll everytime be syntaxed following that you chosed convention.<br>

**Formatter** is useful to modifying syntaxicaly code automatically (or manually).<br>

Example :

With a function declared like this : 
```js
function init({ option1, option2, option3, option4, option5, option6, option7 }) {  
   
}   
```

If you use **formatter** on this file, **formatter** output will be something like this : 
```js
function init ({   
option1,   
option2,    
option3,   
option4,   
option5,   
option6,   
option7   
}) {

}   
```

## How to use, Prettier Example <a id='how-use'></a>

**Prettier** can be used differents ways :

1) VSCode extension (Pretty most easier way)
    - Installing firstly the 'prettier' extension
    - Press Ctrl + Shift + I 

File will be formated automatically following chosed convention

Note: You're able to manage the extension settings, and so manage your prettier configuration

2) Commande Line Interface<br>
    Installing 'prettier' in targeted node environmement (Or installing prettier globaly using _-g_ flag)<br>
    At project root: 
    -   ```sh
        npm init  # Init node in this folder 
        ```
    Installing prettier
    -   ```sh
        npm install --save-dev --save-exact prettier # Installing prettier (You can add the '-g' flag for global installation)
        ```
    If prettier installed locally (only for this project) use this :
    -   ```sh
        npx prettier index.js # Display formated file output as plain text in terminal
        ```
    Else, prettier installed globally, use this :
    -   ```sh
        prettier index.js # Display formated file output as plain text in terminal
        ```
    Another option could interest you, modifying your code with the command line, so use 
    -   ```sh
        npx prettier index.js --write # Replace content of file with formated prettier output
        ```
    Formating all files (in folder) : 
    -   ```sh
        npx prettier --write # Replace content of all files with formated prettier output
        ```
    To check the state of files, you could use : 
    -   ```sh
        npx prettier --check
        ```
    Note: You cannot use --check flag and --write in same time.<br>
    The ```no-config``` flag will force prettier to use basic configuration.<br>
    Some more flags are availables at <a href='#sources'>sources</a>¹ section

## How to configure Prettier <a id='config-prettier'></a>

This example will used the 'air_bnb' convention.<br>

1) Global installation
    Prettier use a file nammed ```.prettierrc``` to manage his configuration.<br>

    In ```.prettierrc``` file (If it doesn't exist, create it with a touch), paste it: 
    ```json
    {  
    "semi": false,  
    "tabWidth": 2,  
    "singleQuote": true  
    }
    ```
2) VSCode extension configuration
    - Check the 'Pretter: semi' case
    - Check the 'Single Quote' case
    - And in 'Prettier: Tab Width' text box, enter wanted value

    It's even possible to acceed at extension configuration file using this command: 
    ```sh
    code . /home/$USER/prettierrc.json
    ```

## Conclusion <a id='conclusion'></a>

Feel free to learn more on formatters by yourself.<br>

## Sources <a id='sources'></a>
<strong>
<a href='https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode'>Prettier - Code Formatter</a><br>
<a href='https://runebook.dev/fr/docs/prettier/cli'>Prettier with CLI</a> <br>
</strong>