
The basis of writing a program in C.

1. The include instructions, must be there for us to use our program.
2. The main block of code with open and close parentheses is called a method.

A method is like a container to put your code and it is what gets executed when we run our programs. E.G looks into the main method and looks into all the codes inside the curly brackets and executes them. 

Whenever you want to run a program you write in C you do 2 things;
- Building a program or compiling a program. 
Build your C file first, with this the code is translated to machine code or computer code so it can execute it.
- Run or execute the program.

At the top of `codeblocks` there is;
- build, 
- run, 
- build & run buttons. 

The semi colon - (`;`) is very important, to end any instruction you write in C. 
`\n` - is a new line character. (I noticed it is the same like python).

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("    /|\n");
    printf("   / |\n");
    printf("  /  |\n");
    printf(" /___|\n");

    return 0;
}
```


> [!NOTE] 
> Order matters - the instructions order matters like if you change any line of the shape, you will get a different output from the above.
> 
> Example of this can be seen below;
> 


```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("    /|\n");
    printf("  /  |\n");
    printf("   / |\n");
    printf(" /___|\n");

    return 0;
}
```

