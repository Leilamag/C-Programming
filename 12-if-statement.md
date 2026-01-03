It is a programming structure which we can use to help our programs make decisions, so in certain circumstances they can respond and do certain things.

## Example

For this example we create a max function to decide which is the biggest number to be retuned to the user.

```c
#include <stdio.h>

int max(int num1, int num2){
    int result;
    if(num1 >= num2){
        result = num1;
    }else result = num2;
}


int main()
{
    printf("%d", max(3,5));
    
    return 0;
}
```

```c
#include <stdio.h>

int max(int num1, int num2){
    int result;
    if(num1 >= num2){
        result = num1;
    }else{ 
        result = num2;
    }
    return result;
}


int main()
{
    printf("%d", max(3,5));
    
    return 0;
}
```

## Max for 3 numbers using if, else if & else

1. Modified the program to spit out the biggest of three numbers when passed to the program;

```c
#include <stdio.h>


int max(int num1, int num2, int num3){
    int result;
    if(num1 >= num2 && num1 >= num3){
        result = num1;
    }else if(num2 >= num1 && num2 >= num3){
        result = num2;
    }else{
        result = num3;
    }
    return result;
}


int main()
{
    printf("%d", max(3,5,14));
    
    return 0;
}
```


> [!NOTE] 
>  || - is a logical operator called `OR`. It allows us to put another condition here in our code.
> 

```c
#include <stdio.h>

int main()
{
    if(3 > 2 || 2 > 5){
        printf("True");
    }
    
    return 0;
}
```

Only one has to be correct or true in the code or statement for it to print `True`. Only one has to be true for it to print `True` in `0R` statement.

> [!NOTE] 
> && - it a logical operator called `AND`. 
> 

```c
#include <stdio.h>

int main()
{
    if(3 > 2 && 2 > 5){
        printf("True");
    } else printf("False");
    
    return 0;
}
```

For `AND` both statement has to be true for it to print `True`.

## Example

```c
#include <stdio.h>

int main()
{
    if(3 > 2 && 2 > 5){
        printf("True");
    } 
    else{ 
        printf("False");
    }
    
    return 0;
}
```

Just a different way to write `if`, `else` from the above code:

```c
#include <stdio.h>

int main()
{
    if(3 > 2 && 2 > 5){
        printf("True");
    } else{
        printf("False");
    }
    
    return 0;
}
```


> [!NOTE] 
> `<` - less than sign
> `>` - greater than sign
> `<=` - less than or equal to sign
> `>=` - greater than or equal to sign
> `==` - equality sign
> `!=` - not equals to 
 > 

## How to negate an entire operation

```c
#include <stdio.h>

int main()
{
    if(!(3 > 2)){
        printf("True");
    }
    
    return 0;
}
```

You will get nothing but when you change the sign above in the below code it works;

```c
#include <stdio.h>

int main()
{
    if(!(3 < 2)){
        printf("True");
    }
    
    return 0;
}
```

So the first code works and print false:


```c
#include <stdio.h>

int main()
{
    if (!(3 > 2)) {
        printf("True\n");
    } else {
        printf("False\n");
    }
    
    return 0;
}
```

# Project

Check if a number is positive, negative, or zero - Number Checker. 
Write a program that takes a number as input and prints whether it's positive, negative, or zero.

```c
#include <stdio.h>

int main()
{
    int number_checker;
    int scan_result;

    printf("Enter your number here: ");
    scan_result = scanf("%d", &number_checker);

    if (scan_result == 1) {  // Successfully read an integer 
        if (number_checker > 0) {
            printf("Number %d is a positive number.\n", number_checker);
        } else if (number_checker < 0) {
            printf("Number %d is a negative number.\n", number_checker);
        } else {  // number_checker == 0
            printf("Number %d is Zero.\n", number_checker);
        }
    } else {
        printf("Invalid number\n");
    }

    return 0;
}
```




