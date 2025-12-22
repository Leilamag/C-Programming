
The `printf` function is an instruction that lets us print things to our screen.
`Printf` - is basically used to find out information, like as you run your programs and you want to find out what they are doing.

The very first code created for us by default from our project;

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("Hello world.\n");

    return 0;
}
```


- With the code below, `world` gets printed in a new line;

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("Hello\nworld.\n");
    return 0;
}
```

## Printing A Single Character

```c
#include <stdio.h>

int main()
{
    int favNum = 1000;
    char myChar = 'a';
    printf("My favorite %s is %c %d", "number", myChar, favNum); 
    return 0;
}
```

## Double quote error

The code below breaks due to the three double quotes;

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("Hello"world.\n");
    
    return 0;
}
```

Escape sequence;
- `\n` - New line.
- `\t` - Tab.
- `\\` - Backslash.
- `\'` - Single quote.
- `\"` - Double quote.
- `\0` - Null character (end of string).

With the code below, `double quotes` gets printed instead of throwing error like one above;

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("Hello\"world.\n");
    
    return 0;
}
```

## Printing Numbers

To print a number you have to use a format specifier. The format specifier means you are telling the `printf` function you want to print out a different type of data that is not plain text like the above.

```c
#include <stdio.h>

int main()
{
    printf("%d", 500); 
    return 0;
}
```

## Printing String With Numbers

```c
#include <stdio.h>

int main()
{
    printf("My favorite number is %d", 500); 
    return 0;
}
```

```c
#include <stdio.h>

int main()
{
    printf("My favorite %s is %d", "number", 500); 
    return 0;
}
```

`%d` -  means you want to print an integer.
`%s` - means you want to include some text.
`%f` - decimal number or a double.
`%c` - this will allow to print a single character.


> [!NOTE] 
> The order you put the "order specifier" in the your code should be the order you include them when using the commas before you close that line of code.
> 

## Printing Doubles or Decimal Number 

```c
#include <stdio.h>

int main()
{
    printf("My favorite %s is %f", "number", 3.142); 
    return 0;
}
```

This is useful when you introduce variables.

```c
#include <stdio.h>

int main()
{
    double favNum = 3.142;
    printf("My favorite %s is %f", "number", favNum); 
    
    return 0;
}
```

OR

```C
#include <stdio.h>

int main()
{
    int favNum = 1000;
    printf("My favorite %s is %d", "number", favNum); 
    
    return 0;
}
```

