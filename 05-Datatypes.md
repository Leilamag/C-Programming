#### For numbers:
- Integers - `int`. 
- Decimal numbers - either `double` or `float`. 

#### Characters:
- char - you put what you want to store inside a single quote. 

```
char <Give The Variable A Name> = 'single character';
```

`Note`: you can only store only one single character here, if more than one it will throw an error. 

- To represent a string meaning not a single character, you can do that with the following or like this below;

```
char <Give The Variable A Name>[] = “multiple characters or string”;
```

Example:

```
char characterName[] = "John";
```

Examples for the major data types below;

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int score = 75;
    double gpa = 3.5;
    char grade = 'A';
    char result[] = "You Passed!";
    
    return 0;
}
```


# Project

Demonstrate the size of different data types - Write a program that prints the size of int, char, float, and double data types using `sizeof`.

```c
#include <stdio.h>

int main()
{
    printf("Size of int: %zu bytes.\n", sizeof(int));
    printf("Size of char: %zu bytes.\n", sizeof(char));
    printf("Size of float: %zu bytes.\n", sizeof(float));
    printf("Size of double: %zu bytes.\n", sizeof(double));
    return 0;
}
```
