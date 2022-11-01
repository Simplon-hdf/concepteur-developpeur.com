# Sommaire

- <a href='#formatters'>Formatters</a>
    - <a href='#wawuf'>What's are and Why use formatters</a>
    - <a href='#how-use'>How use, Prettier Example</a>
    - <a href='#config-prettier'>How to configure Prettier</a>
- <a href='#conclusion'>Conclusion</a>

## Formatters

### What's are and why use Formatters <a id='wawuf'></a>

**Formatter** is a useful tool for following code conventions, with formatter you'll be able to modify your code to match with chosed code convention.<br>
That way, your code'll everytime be syntaxed following that you chosed convention.<br>

**Formatter** is useful to modifying syntaxicaly code automatically (or manually).<br>

Example :

With a function declared like this : 
```
function init({ option1, option2, option3, option4, option5, option6, option7 }) {  
   
}   
```

If you use **formatter** on this file, **formatter** output will be something like this : 
```
funtion init ({   
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