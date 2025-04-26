---
date: 2025-04-24T22:59
tags:
  - C
cssclasses:
  - page-manila
  - center-titles
---
# Operators and Expressions

## Arithmetic Operators

There are 7 arithmetic operators mainly used in C. Those are:
- Addition (+)
- Subtraction (-)
- Multiplication (\*\)
- Division (/)
- Modulus (%)
- Increment (++)
- Decrement (--)

```c
int x = 5;
int y = 4;

int a = x + y;
int b = x - y;
int c = x*y;
float d = x / y; // When dividing 2 integers, the decimal portion will be 0's
// To solve this, we can type either of the 2 things
// Convert 'y' into a float or double in the operation itself and not change the original datatype
float e = x / (float) y;
// OR you can convert 'y' into a float or double like this
float y = 4;

int f = x % y;
x++; // Adds 1 to it
y--; // Subtracts 1 to it
```

You can also use operators on the same variable just like Python.
```c
int x += 1;
// It is the same as
int x = x + 1
// Other operators are
int x -= 1;
int x *= 1;
int x /= 1;
int x %= 1; // When divided by 1, output is always 0.
```

## Logical Operators

These are mostly used in `if` statements.

1. `AND` operator
```c
temp >= 0 && temp <=30;
```

2. `OR` Operator
```c
temp >= 0 || temp <=30;
```

3. `NOT` Operator
```c
!temp // !<variable>
```
