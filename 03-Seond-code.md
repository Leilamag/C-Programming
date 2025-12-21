# Drawing shapes

Let us draw a triangle.

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

# Problem

Renamed the `main.c` for orderliness to `2.Hello-World.c`. So in my project folder - I can create each topic file's, for the next topic Building shapes (I created new file and called it `3. Second-Code.c`) and so on. 

But it's going to be tricky or not just straight forward like `python` where you can have various or different files in one project and have them run with ease.  

In C, **a program/Project can have only ONE `main()` function**:
You can not just create a new C file in this project (and give or name it - `3. Second-Code.c` and so on) you would run into `main()` function issue or error. 

## Solution 1: 
One `main()` per project (BEST for beginners) - Create **a separate project for each program**.

## Solution 2: 
Exclude a file from build (Code::Blocks) - If you want to keep files but compile only one:

1. Right-click the `.c` file you want to exclude and in this case the main or hello file.
2. Choose `Properties`.
3. Uncheck `Compile file` and `Link file`.
4. Build again.

## Solution 3: 
Remove `main()` from one file - If both files must stay in the same project:
- Keep `main()` in **only one file**
- Change the other file to contain **functions only**

Main code - `2.Hello-World.c`;

```c
#include <stdio.h>
#include <stdlib.h>

void shapes(void);

int main()
{
    printf("Hello world!\n");
    shapes();
    return 0;
}
```

Second file - `3.Second-Code.c`;

```c
#include <stdio.h>

void shapes(){
    printf("    /|\n");
    printf("   / |\n");
    printf("  /  |\n");
    printf(" /___|\n");

}
```


## Solution 4: 
Creating header and the new C file.

`.c` + `.h` - This is how **real C projects** are structured.

Main code - `2.Hello-World.c`;

```c
#include <stdio.h>
#include <stdlib.h>
#include "header.h"

int main()
{
    printf("Hello world!\n");
    shapes();
    return 0;
}
```

Header file: create one - `header.h`;

```
#ifndef SECOND_CODE_H_INCLUDED
#define SECOND_CODE_H_INCLUDED

void shapes(void);

#endif // SECOND_CODE_H_INCLUDED
```

Second C file you want to also run  - `3.Second-Code.c`;


```c
#include <stdio.h>
#include "header.h"

void shapes(void) {
    printf("I'm drawing a traiangle below\n");
    printf("\n");
    printf("    /|\n");
    printf("   / |\n");
    printf("  /  |\n");
    printf(" /___|\n");
    printf("\n");
    printf("I'm drawing a rectangle below\n");
    printf("\n");
    printf(" ________________\n");
    printf("|                |\n");
    printf("|                |\n");
    printf("|________________|\n");
}
```




