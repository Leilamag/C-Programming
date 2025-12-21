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

# The basis of writing a program in C.

1. The include instructions, must be there for us to use our program which are known as preprocessor directives.
Preprocessor Directives - these are instructions to the compiler, telling it to include specific header files before compiling the code.
- `#` - is used for preprocessor directives, like `#include`, `#define`, `#ifdef` etc.
In python, `#` is used for commenting, but in C, it is used for preprocessor directives, different language different rules.

`#include <stdio.h>` - include standard input/output: This header file provides functions for input/output operations `i.e` 
- `printf()` - for printing output
- `scanf()` - for reading input
- `getchar()` - for reading characters
- `putchar()` - for writing character etc.

`#include <stdlib.h>` - include standard library: This header file provides general-purpose functions `i.e` 
- Memory management - `malloc()`, `calloc()`, `realloc()`, `free()`.
- Process control - `exit()`, `baort()`.
- String conversion - `atoi()`, `atol()`, `strtol()`.
- Random number generation - `rand()`, `strand()`.

## Why include these headers;
Including these headers allows you to use the functions they  provide. If you do not include them, the compiler would not know what those functions are and you will get errors.

In modern C, it is recommended we use `#include <stdio.h>` instead of `#include "stdio.h"` for standard library header.


2. The main block of code - `main()` with open and close curly parentheses is called a method.

A method is like a container to put your code and it is what gets executed when we run our programs. `etc` looks into the main method and looks into all the codes inside the curly brackets and executes them

The semi colon - (`;`) is very important, to end any instruction you write in C. 

`\n` - is a new line character. (I noticed it is the same like python).

# Running a program

Whenever you want to run a program you write in C you do 2 things;
- Building a program or compiling a program. 
Build your C file first, with this the code is translated to machine code or computer code so it can execute it.
- Run or execute the program.

## CodeBlock Application

At the top of `codeblocks` there is;
- build, 
- run, 
- build & run buttons. 



