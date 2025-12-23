It is a special block of code in C that get's ignored when you run your program.
Comments are you use to:
- explain a certain line of code or 
- to comment out a line of code instead deleting the line of code.


In C `#` is not used for commenting lines of code like it is, in python - here it is used for preprocessor directives.

## Method 1

`//` - is used for single-line comments

To start a comment you can also use two (2) forward slash `//`.

```c
#include <stdio.h>
#include <stdlib.h>


int main()
{
    //This is my first comment in C language
    
    printf("This is my first comment in C\n");
    printf("Comments are fun");
    
    return 0;
}
```


## Method 2

`/*  */`  - is used for multi-line comments.

```
/*

Comment goes here
 
*/
```

To start a comment you use a forward slash `/` and asterisk `*` to open the comments and to close you use asterisk  `*` and forward slash `/`.

```c 
#include <stdio.h>
#include <stdlib.h>


int main()
{
    /* This is my Second comment in C language */
    
    printf("This is my Second comment in C\n");
    printf("Comments are fun");
    
    return 0;
}
```



> [!NOTE] 
> Only use a comment when you have to or when necessary - for best practice.


