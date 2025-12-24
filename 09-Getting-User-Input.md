
This prompt the user to enter some information and also you can store in a variables.
`scanf` function - is used or allow the user to enter/input some information into the program.

## To Get Integer

For this example we used age;

```c
#include <stdio.h>

int main()
{
    int age;
    printf("Enter your age: ");
    scanf("%d", &age);
    printf("You are %d years old", age);
    
    return 0;
}
```

The ampersand - `&` :  is like a pointer.
`&age` - is where age lives in memory.
To store the integer value or number entered in age variable. The ampersand lets you get input from the user.

## To Get Decimal

Decimal - Float or Double.
For this example we use `gpa`;

```c
#include <stdio.h>

int main()
{
    double gpa;
    printf("Enter your gpa: ");
    scanf("%lf", &gpa);
    printf("Your gpa is %f", gpa);
    
    return 0;
}
```


> [!NOTE] 
> We use the `%lf` in the `scanf` function to tell the `scanf` function we are looking for a double.
> 
> Recall format specifier;
> 
> - `%c` - for a single character/letter.
> 
> - %s - for a string/text.
>  
> - %d - for an integer.
>  
> - `%f` - for a decimal number/floating point numbers.
>  
> - `%lf` - for a double.
>   

## To Get Character

Character - a single letter or character.
For this example we are going use `grade`;

```c
#include <stdio.h>

int main()
{
    char grade;
    printf("Enter your grade: ");
    scanf("%c", &grade);
    printf("Your grade is %c", grade);
    
    return 0;
}
```

## To Get String

To get a string of character's from the user;
For this example we are going use `name`;

```c
#include <stdio.h>

int main()
{
    char name[20];
    printf("Enter your name: ");
    scanf("%s", &name);
    printf("Your name is %s.\n", name);
    return 0;
}
```


> [!NOTE] 
> Whenever you are creating a string character you need the open and close square brackets `[]`.
> You should specify the number of characters in the open and close square brackets `i.e` if 30. So C can know how big the variable characters would be.
> 

### Error - Two names cannot Returned

If you enter two (2) names like the following below;
  
```input
John Mark
```

You will get the error just the first name before the first spacing outputted, instead of outputting both names inputted which is `John Mark` , we get only `John`;

```result
Your name is John
```

Like it did below with the result below;

```results
Enter your name: John Mark
Your name is John.

Process returned 0 (0x0)   execution time : 5.194 s
Press any key to continue.
```

This is a problem with using the `scanf` when trying to get a string from a user it will grab all characters before the first space. 
You can modify `scanf` to get the whole line with spaces or the entire string inputted or you can use the `fgets` function to solve this.

#### Solution 1 - `scanf with a scanset`

You can use a `scanset` to read a string with spaces - this reads everything until a newline (`\n`).

```example
scanf("%[^\n]", name);
```

`%[^\n]`: This is a `scanset`, a special type of format specifier. A proper breakdown of what it does;

- `^` -  Means "not" or "except".
- `\n` -  The newline character.

So, `%[^\n]` reads everything until a newline (`\n`) is encountered. So it reads the entire line, including spaces, but stops at the newline.

```c
#include <stdio.h>

int main()
{
    char name[20];
    printf("Enter your name: ");
    scanf("%[^\n]", &name);
    printf("Your name is %s.\n", name);
    return 0;
}
```

#### Not A Solution - `scanf with a width specifier`

You can specify a maximum width to avoid buffer overflow:

```
scanf("%49s", name); // assumes name is char name[50]
```

A proper breakdown of what it does;

- `%49s`: Reads a string with a maximum width of 49 characters.
- Leaves space for the null terminator (`\0`).

> [!NOTE] ISSUE
> Still stops at whitespace (spaces, tabs, etc.), so not ideal for reading full names with spaces.

```c
#include <stdio.h>

int main()
{
    char name[20];
    printf("Enter your name: ");
    scanf("%19s", name); // assumes name is char name[20]
    printf("Your name is %s.\n", name);
    return 0;
}
```

Still get the error of just the first name before the first spacing outputted, instead of outputting both names inputted which is `John Mark`.


#### Solution 2 - `fgets`.

`fgets` - reads the entire line, including spaces, until it hits a newline or the buffer is full.

```example
fgets(name, 20, stdin);
```

```c
#include <stdio.h>

int main()
{
    char name[20];
    printf("Enter your name: ");
    fgets(name, 20, stdin);
    printf("Your name is %s", name);

    return 0;
}
```

	OR

`sizeof(name)` - as seen below

```
fgets(name, sizeof(name), stdin);
```

```c
#include <stdio.h>

int main()
{
    char name[20];
    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin);
    printf("Your name is %s", name);

    return 0;
}
```

Now we get both names without having the first spacing encountered issues outputted. `fgets` grabs the whole line of text you input.

> [!NOTE] 
> Both codes above do the same thing
> 

```result
Enter your name: John Mark
Your name is John Mark

Process returned 0 (0x0)   execution time : 4.959 s
Press any key to continue.
```


> [!NOTE] 
> When using `fgets` the first thing or argument you specify is the name of the variable you want it to store your text.
> With this `fgets` you must specify the number of characters of input from user (to be inputted by the user) to avoid overflowing the buffer, so the C program does not break.
> 
> `stdin` - stands for standard input. This is where we are going to get the information from or it is like the console you are using or typing your input on.
> 

##### Note `fgets` issue

We can see the problem in the following code below;

> [!NOTE] 
> The downside of the `fgets` function is that it enters a new line characters, as you can see below, after printing the complete name we gave the program it continues the output of the code/program in a newline.
> 
> So you should be aware of this.

```c
#include <stdio.h>

int main()
{
    char name[20];
    int age;
    printf("Enter your name: ");
    fgets(name, 20, stdin);
    printf("Enter your age: ");
    scanf("%d", &age);
    printf("Your name is %s and you are %d years old.\n", name, age);
    return 0;
}
```

As we see can see here;

```result
Enter your name: mr love
Enter your age: 23
Your name is mr love
 and you are 23 years old.

Process returned 0 (0x0)   execution time : 4.534 s
Press any key to continue.
```

> [!NOTE] FIX
> To fix this - while still using `fgets`:
> You remove the newline using `strcspn` and the preprocessor directive of `<string.h>` as seen below.
> 
> `strcspn` is part of the C standard library (`string.h`), and it's used to find the length of the initial segment of a string that doesn't contain certain characters (in this case, `\n`).
> 

For now, you can just know that the example or mini code below  is a common trick to remove the newline character from a string read with `fgets`.

```example
#include <>string.h

name[strcspn(name, "\n")] = 0; // remove newline
```

New and correct code:

```c
#include <stdio.h>
#include <string.h>

int main()
{
    char name[20];
    int age;
    printf("Enter your name: ");
    fgets(name, 20, stdin);
    name[strcspn(name, "\n")] = 0; // remove newline
    printf("Enter your age: ");
    scanf("%d", &age);
    printf("Your name is %s and you are %d years old.\n", name, age);
    return 0;
}
```


> [!NOTE] 
> Solution 1 - `scanf with a scanset`
> 
> Not A Solution - `scanf with a width specifier`
> 
> Solution 2 - `fgets`
> 
> `fgets` is usually the simplest and safest choice
> 


# Tweaking or Playing around the return value

Whatever number you specify here is what gets return when the code/program exit or is done running. The reason it worked is because in C, the return value of the `main()` indicates the program exit status to the OS.

```
return 0;  //this typically means success
```

So when it gives a non zero value this typically means error.

In C, return expects an `int` value from the `main()`, so you cannot directly return a letter or single character like 'a'.
If you try `return 'a';` - it will work but:
- `'a'` - is treated as an `int` (its ASCII value, 97).
- So `return 'a';` - is like `return 97;`.

```
return 'a';  //returns 97
```

 Or a string like `'aa'`:

```
return 'aa';  //Process returned 24929
```

# Project

Ask for user's name and greet them - create a program that asks for the user's name and prints a personalized greeting.

Using `fgets` which would read the entire line;

```c
#include <stdio.h>
#include <string.h>

int main()
{
    char username[30];
    printf("Can you enter your instagram's username below\n>>> ");
    scanf("%[^\n]", &username);
    username[strcspn(username, "\n")] = 0;
    printf("Welcome to instagram %s!!!\n", username);
    return 0;
}

```




