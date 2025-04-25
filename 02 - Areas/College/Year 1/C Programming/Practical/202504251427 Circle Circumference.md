---
date: 2025-04-25T14:27
tags:
  - C
  - Practical
cssclasses:
  - page-blueprint
---
# Circle Circumference Program

```c
#include <stdio.h>
#include <math.h>

int main(){
    const float pi = 3.14159;
    float radius;
    printf("Hello, this program calculates the circumference of a circle using the given radius.");
    printf("\nType the radius of the circle in centimeters:");
    scanf("%f", &radius);
    
    double circumference = 2*pi*radius;
    printf("The area of the circle is %0.3lf cm.", circumference);
    
    return 0;
}
```

Output:
```text
Hello, this program calculates the circumference of a circle using the given radius.
Type the radius of the circle in centimeters:10
The area of the circle is 62.832 cm.

...Program finished with exit code 0
```