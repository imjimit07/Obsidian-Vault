---
date: 2025-04-24T23:23
tags:
  - C
cssclasses: []
---
# LIBRARY FUNCTIONS: INPUT, OUTPUT, MATHEMATICS, DATE AND TIME

## User Input

To accept user input and print it, type this:
```c
#include <stdio.h>
#include <string.h> // Removes the newline character in the end

int main(){

	char name[25]; // bytes
	char fullname[25];
	int age;

	printf("\nWhat is your name?");
	scanf("%s", &name); // read up to a white space and will include the newline character

	printf("\nHow old are you?");
	scanf("%d", &age);

	printf("\nWhat is your full name?");
	fgets(fullname, 25, stdin);
	name[strlen(name)-1] = '\0'; // Also helps in removeing the newline character

	printf("Hello %s", fullname);
	printf("Hello %s", name);
	printf("You are %d years old.", age);
	
	return 0;
}
```

## Math Functions

To use math functions, type this on the top of the code:
```c
#include <math.h>
```

1. Square Root
```c
double A = sqrt(9);
```

2. Powers
```c
double B = pow(2, 4); // 2^4 = 16
```

3. Rounding Off
```c
int C = round(3.14);
```

4. Round Up
```c
int D = ceil(3.14); // Answer is 4
```

5. Round Down
```c
int E = floor(3.99); // Answer is 3
```

6. Absolute Value
```c
double F = fabs(-100); // Answer is 100
```

7. Logarithm
```c
double G = log(3);
double G = log2(3); // Base 2
```

8. Trigonometry
```c
double H = sin(35);
double I = cos(35); // All in RADIANS
double J = tan(35);
```

9. Floating Point Remainder
```c
double K = fmod(11.0, 3.0) // Output is 2.00000
```

## Time and Clock

The `time()` function gives the time since 00:00:00 UTC 1 January 1970. This function can be used by typing this on top of the file:
```c
#include <time.h>
```

To print the seconds passed since 1 January 1970, type this:
```c
time_t time( time_t *second )
```

Where `time_t` is datatype used to represent the seconds passed since 1 January 1970.

Example Program (GeeksforGeeks)
```c
// C program to demonstrate
// example of time() function.
 
#include <stdio.h>
#include <time.h>
 
int main()
{
    time_t seconds;
 
     // Stores time seconds
    time(&seconds);
    printf("Seconds since January 1, 1970 = %ld\n", seconds);
 
    return 0;
}
```

Output:
```text
Seconds since January 1, 1970 = 1538123990
```

A `difftime()` function is used to calculate the difference between 2 given times (in seconds). The output is always in seconds.

Syntax:
```c
double difftime(time_t time2, time_t time1);
```

Both times are the number of seconds from 1 January 1970.

A `clock()` is used to calculate the processor time taken by the program.

