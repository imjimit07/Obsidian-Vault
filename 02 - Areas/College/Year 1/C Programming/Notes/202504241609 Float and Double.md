---
date: 2025-04-24T16:09
tags:
  - C
cssclasses:
  - page-manila
  - center-titles
---
# Float and Double

When printing a **float and double**, the system only prints first 6-7 digits of the decimal.

To print more digits, type this:
```c
printf("%0.15lf", variable); // This will print first 15 decimal places
```

In this example, I printed both float and double variables having the same decimal. We can see a difference in the value of the decimal printed after 5-6 digits.
```c
#include <stdio.h>

int main() {
     float simpledecimal = 1.569237562837543;
     double precisedecimal = 1.569237562837543;
     
     printf("%0.15f\n", simpledecimal);
     printf("%0.15lf", precisedecimal);

    return 0;
}
/*
Output:

1.569237589836121
1.569237562837543
*/
```

This is due to the storage taken by the double variable.
> More Storage = More Precision!