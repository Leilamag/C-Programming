Constants is a special type of variable in C which cannot be modified - it is like a "read-only" variable - it cannot be modified after initialization. 

A constant can refer to any text or number that you are using in your program. A piece of information or data  in your program that is unchanging unless you manually come into the code and modify the code, so this is considered a constant. 
When you create constants in C, you are creating a value that is/will be unable to be modified.

For example, the code below we can see the variable `num` gets modified when given the value 8:
#### Error

Without the new line character in our code, we can see the output or result as 58, instead of the 5 and 8 separate;

```c
#include <stdio.h>

int main()
{
    
    int num = 5;
    printf("%d", num);
    num = 8;
    printf("%d", num);
    
    return 0;
}
```

##### Output to the above code

```result
58
Process returned 0 (0x0)   execution time : 0.053 s
Press any key to continue.
```

Lol like as if we mean to print 58.

#### Correct code - to show how the num variable is modified

```c
#include <stdio.h>

int main()
{
    
    int num = 5;
    printf("%d\n", num);
    num = 8;
    printf("%d\n", num);
    
    return 0;
}
```

# Constants

A constant as already defined can refer to any text or number that you are using in your program.
A piece of information or data  in your program that is unchanging unless you manually come into the code and modify the code, so this is considered a constant. 

The above is explained in the example's below, with codes like these:

```c
#include <stdio.h>

int main()
{
    printf("Hello");
    
    return 0;
}
```

You have to enter or edit the code manually;

```c
#include <stdio.h>

int main()
{
    printf("%d", 70);
    
    return 0;
}
```

Let’s say I do not want the number 5 to be able be modified, I will use `const` keyword.
You can use the `const` right before you declare the variable type - for example `int`;

```
const int num = 5
```

Or after you declared the type;

```
int const num = 5
```

## Example

```c
#include <stdio.h>

int main()
{
    
    const int num = 5;
    printf("%d\n", num);
    num = 8;
    printf("%d", num);
    
    return 0;
}
```

With the above code you will get an error - when I tried to build and run, since `num` variable could not be modified when a `num` value was assigned 8.

```result
||=== Build: Debug in Project (compiler: GNU GCC Compiler) ===|
main.c||In function 'main':|

main.c|7|error: assignment of read-only variable 'num'|
||=== Build failed: 1 error(s), 0 warning(s) (0 minute(s), 0 second(s)) ===|
```

From any of these online C compilers;

- [`Onlinegdb`](https://www.onlinegdb.com/online_c_compiler)
- [`Onecompiler`](https://onecompiler.com/c/448egjh6p)

Got the following below;

```result
main.c: In function ‘main’:
main.c:8:9: error: assignment of read-only variable ‘num’
    8 |     num = 8;
      |
      
```


> [!NOTE] 
> You can use uppercase letter for the variables of constant for best practices.

# Project

Calculate the area of a circle using a constant for pi - Define a constant for pi (3.14) and use it to calculate the area of a circle given a radius.

```c
#include <stdio.h>

int main()
{

    const float pi = 3.14;
    int radius = 8;
    //we used float keyword since the result is going to be a decimal number.
    float area = pi * radius * radius;
    printf("%f\n", area);

    return 0;
}
```

