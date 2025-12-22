Variables in `C` is essentially a container to store different pieces of information or data values `etc` text, numbers or characters. 

A simple program below;

```c
#include <stdio.h>

int main()
{
    printf("There once was a man named George.\n");
    printf("he was 70 years old.\n");
    printf("He really liked the name George.\n");
    printf("but did not like being 70.\n");

    return 0;
}
```

A variable is declared as;

```
dataType variable_name;
```

Primary data types are;
- `char` - 8-bit signed numbers.
- `int` - 32-bit signed numbers.
- `float` - 32-bit signed single-precision fractional real numbers.
- `double` - 32-bit signed double-precision fractional real numbers.
Variables belonging to the same data type can be defined on the same line;

```
dataType variable_name1, variable_name2;
```

To avoid the stress of looking through the entire program to change the `name` or `age`, you can use variable to keep track and manage this information.

```c
#include <stdio.h>

int main()
{
    char characterName[] = "Abram";
    int characterAge = 35;
    printf("There once was a man named %s.\n", characterName);
    printf("He was %d years old.\n", characterAge);
    printf("He really liked the name %s.\n", characterName);
    printf("But did not like being %d.\n", characterAge);

    return 0;
}
```


> [!NOTE] 
> We can see the name changed from `George` to `Abram` and age also from 70 to 35 from the original code.
> 
> %s - is like a place holder for the string or to insert a string there. 
> %d - means insert an integer there.
> 

You can modify the information stored halfway, like below;

```c
#include <stdio.h>

int main()
{
    char characterName[] = "Abram";
    int characterAge = 35;
    printf("There once was a man named %s\n", characterName);
    printf("He was %d years old.\n", characterAge);
    
    characterAge = 100;
    printf("He really liked the name %s\n", characterName);
    printf("But did not like being %d.\n", characterAge);

    return 0;
}
```

Notice the result below;

```result
There once was a man named Abram 
He was 35 years old. 
He really liked the name Abram 
But did not like being 100.
```


# Project

Create a program that prints your information stored by it and a greeting with these info, maybe;
- your name
- age
- Country

```c
#include <stdio.h>

int main()
{
    char myName[]= "Philip";
    int myAge = 29;
    char Country[]= "Nigeria";
    printf("Hello %s, so you are from %s.\n", myName, Country);
    printf("I can see your age is %d and you are too old to learn C, LOL just kidding!\n", myAge);
    printf("Nevertheless I hope you enjoy the journey.\n");
    return 0;
}
```

