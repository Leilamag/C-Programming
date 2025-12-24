

```c
#include <stdio.h>

int main()
{
    printf("%f", 8.9); 
    return 0;
}
```

> [!NOTE] 
> Math with a floating point number and integer would give you a floating point number.
> 

# With Variables

```c
#include <stdio.h>

int main()
{
    int num = 7;
    printf("%d", num); 
    return 0;
}
```

# Addition

```c
#include <stdio.h>

int main()
{
    printf("%f", 5.0 + 4.5); 
    return 0;
}
```

Example 2:

```c 
#include <stdio.h>

int main()
{
    printf("%f", 5 + 4.5); 
    return 0;
}
```

# Subtraction

```c
#include <stdio.h>

int main()
{
    printf("%f", 5.0 - 4.5); 
    return 0;
}
```

# Division

```c
#include <stdio.h>

int main()
{
    printf("%f", 5.0 / 4.5); 
    return 0;
}
```

# Multiplication

```c
#include <stdio.h>

int main()
{
    printf("%f", 5.0 * 4.5); 
    return 0;
}
```


# Errors & Corrections

Observe the code below, the result is incorrect due to the fact it printing of integer format specifier - `%d`.

```c
#include <stdio.h>

int main()
{
    printf("%d\n", 5 / 4); 
    printf("%d", 1 / 2); 
    return 0;
}
```

```result
1
0
Process returned 0 (0x0)   execution time : 0.093 s
Press any key to continue.
```

Now with floating specifier;

> [!NOTE] 
> Just add a decimal or point to any of the numbers before and then use the floating number format specifier.
> 

```c
#include <stdio.h>

int main()
{
    printf("%f\n", 5 / 4.0); 
    printf("%f", 1 / 2.0); 
    return 0;
}
```

```result
1.250000
0.500000
Process returned 0 (0x0)   execution time : 0.072 s
Press any key to continue.
```

# Complex Math Functions

Notice, I have to include the `math.h` at the top.

`pow - cube` 

```c
#include <stdio.h>
#include <math.h>

int main()
{
    printf("%f",pow(2,3) ); 
    return 0;
}
```

`sqrt - squareroot` 

```c
#include <stdio.h>
#include <math.h>

int main()
{
    printf("%f",sqrt(36) ); 
    return 0;
}
```

`ceil - round up`
- Returns the **smallest integer value that is greater than or equal to** the number.
- The return type is `double`.

```c
#include <stdio.h>
#include <math.h>

int main()
{
    printf("%f", ceil(36.756) ); 
    return 0;
}
```

`floor - round down`
- Returns the **largest integer value that is less than or equal to** the number.
- The return type is `double`.

```c
#include <stdio.h>
#include <math.h>

int main()
{
    printf("%f", floor(36.756) ); 
    return 0;
}
```

> [!NOTE] 
> Observe the difference from the rounding up or down from the ceil and floor example above.
> 
> Google C `maths` functions and play around with them
> https://en.wikipedia.org/wiki/C_mathematical_functions
> 

# Project


```
#include <stdio.h>
#include <math.h>

int main() {
    double x = -4.7;

    printf("ceil: %.0f\n", ceil(x));
    printf("floor: %.0f\n", floor(x));
    printf("round: %.0f\n", round(x));
    printf("sqrt: %.2f\n", sqrt(16));
    printf("pow: %.2f\n", pow(2, 3));

    return 0;
}
```




