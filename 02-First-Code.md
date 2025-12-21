# Creating our project - C Programming.
Run the `codeblocks` application;
1. Start a new a project by clicking on the `Create a new project` on your screen or click on file and select new project. 
2. Select `Console application`. 
3. Select C. 
4. Give a name - `C Programming` for the new project.
5. Saved project to any folder on your desktop. 
6. Leave the next setup window as default and click finish.

Once the projects is created and started:
- There is a `main.c` file in the source folder, it was created by default with `codeblocks`.

Code found in the `main.c` file;

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("Hello World");

    return 0;
}
```

- Click the `Build and run` icon to run the file or execute the program.

# Problem

Renamed the `main.c` for orderliness to `2.Hello-World.c`. So in my project folder - I can create each topic file's, for the next topic Building shapes (I created new file and called it `3. Second-Code.c`) and so on. 

But it's going to be tricky or not just straight forward like `python` where you can have various or different files in one project and have them run with ease.  

In C, **a program can have only ONE `main()` function**:
You can not just create a new C file n this project and give or name it - `3. Second-Code.c` and so on, you would run into `main()` function issue or error. 

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
    printf("    /|\n");
    printf("   / |\n");
    printf("  /  |\n");
    printf(" /___|\n");
}
```


