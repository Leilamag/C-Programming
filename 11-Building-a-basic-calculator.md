Building a basic calculator that takes just two(2) numbers and gives the value or answers for addition, subtraction, multiplication and division.

```c
#include <stdio.h>

int main()
{
    int num1;
    int num2;
    printf("Enter first number: ");
    scanf("%d", &num1);
    printf("Enter second number: ");
    scanf("%d", &num2);

    printf("\nAnswer for addition: %d\n", num1 + num2);
    printf("Answer for subtraction: %d\n", num1 - num2);
    printf("Answer for multiplication: %d\n", num1 * num2);
    printf("Answer for division: %d", num1 / num2);

    return 0;
}
```

```results
Enter first number: 10
Enter second number: 2
Answer for addition: 12
Answer for subtraction: 8
Answer for multiplication: 20
Answer for division: 5
Process returned 0 (0x0)   execution time : 2.781 s
Press any key to continue.
```

The problem with the above addition calculator is that, it does only integer you cannot get correct answer from decimal calculations.
Below is the result when I tried adding an a float number to an integer;

```result
Enter first number: 10
Enter second number: 2.5

Answer for addition: 12
Answer for subtraction: 8
Answer for multiplication: 20
Answer for division: 5
Process returned 0 (0x0)   execution time : 5.935 s
Press any key to continue.
```

To solve the above, yo modify the code below with variable type of float using `double`;

```c
#include <stdio.h>

int main()
{
    double num1;
    double num2;
    printf("Enter first number: ");
    scanf("%lf", &num1);
    printf("Enter second number: ");
    scanf("%lf", &num2);

    printf("\nAnswer for addition: %f\n", num1 + num2);
    printf("Answer for subtraction: %f\n", num1 - num2);
    printf("Answer for multiplication: %f\n", num1 * num2);
    printf("Answer for division: %f", num1 / num2);

    return 0;
}
```

Trying int number of 10 and a float number of 2.5, got the correct result;

```result
Enter first number: 10
Enter second number: 2.5

Answer for addition: 12.500000
Answer for subtraction: 7.500000
Answer for multiplication: 25.000000
Answer for division: 4.000000
Process returned 0 (0x0)   execution time : 5.261 s
Press any key to continue.
```

The above calculator is not secured though, it will break if you run or enter a string of characters instead of a number.

Trying a string of characters `dd`, the program breaks below;

```results
Enter first number: dd
Enter second number:

Answer for addition: 0.000000
Answer for subtraction: 0.000000
Answer for multiplication: 0.000000
Answer for division: -nan(ind)
Process returned 0 (0x0)   execution time : 2.427 s
Press any key to continue.
```

