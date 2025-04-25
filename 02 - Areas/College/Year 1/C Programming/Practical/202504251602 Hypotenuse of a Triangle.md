---
date: 2025-04-25T16:02
tags:
  - C
  - Practical
cssclasses:
  - page-blueprint
---
# Hypotenuse of a Triangle

```c
#include <stdio.h>
#include <math.h>

int main(){
    float base;
    float height;
    printf("Hello, this program calculates the hypotenuse of a triangle using the given sides.");
    printf("\nType the length of the base of the triangle in centimeters:");
    scanf("%f", &base);
    printf("\nType the length of the height of the triangle in centimeters:");
    scanf("%f", &height);
    
    double hypotenuse = sqrt(pow(base, 2)+pow(height, 2));
    printf("The length of the hypotenuse of the triangle is %0.3lf cm.", hypotenuse);
    
    return 0;
}
```

Output:
```text
Hello, this program calculates the hypotenuse of a triangle using the given sides.
Type the length of the base of the triangle in centimeters:2 

Type the length of the height of the triangle in centimeters:3
The length of the hypotenuse of the triangle is 3.606 cm.

...Program finished with exit code 0
```
