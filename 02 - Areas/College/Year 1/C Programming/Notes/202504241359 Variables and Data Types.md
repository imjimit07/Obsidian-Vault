---
date: 2025-04-24T13:59
tags:
  - C
cssclasses:
  - center-images
---
# CONSTANTS, VARIABLES, AND DATA TYPES

## Variables

- Used to allocate space to store a value.
- Easier to access the value using the variable name.
- **BUT** we have declare the type of data we are storing with the variable.

To create a variable, type this:
```c
int x; // declaration
x = 123;
int y = 321; //declaration and initialization
int age = 21; //integer
float gpa = 2.05; // float point number
char name = 'J'; // char stores a single character
char name[] = "Jimit"; // this store more than 1 letter and use double qoutes only
```

To print variables in a ‘printf()’ statement, type this:
```c
printf("You are %d years old!", age); // %d - decimal
printf("Your name is %s.", name); // %s - string
printf("Your name is %c.", name); // %c - character
printf("Your name is %f.", gpa); // %f - float
```

## Data Types

| Data Type                                                   | Size (Bytes)             | Range                                   | Format Specifier                         |
| ----------------------------------------------------------- | ------------------------ | --------------------------------------- | ---------------------------------------- |
| signed char                                                 | 1                        | -128 to 127                             | %c or %d<br>[[202504241610 signed char]] |
| unsigned char                                               | 1                        | 0 to 255                                | %c                                       |
| array of characters                                         | unlimited                | unlimited                               | %s                                       |
| float                                                       | 4 (32 bits of precision) | 1.2E-38 to 3.4E+38                      | %f                                       |
| int<br>6-7 digits                                           | 4                        | -2,147,483,648 to 2,147,483,647         | %d                                       |
| unsigned int<br>9-10 digits                                 | 4                        | 0 to 4,294,967,295                      | %u                                       |
| double<br>15-16 digits<br>[[202504241609 Float and Double]] | 8 (64 bits of precision) | 1.7E-308 to 1.7E+308                    | %lf                                      |
| bool (boolean)                                              | 1                        | 0-1 (Prints 0 for False and 1 for True) | %d                                       |
| short                                                       | 2                        | -32,768 to 32,767                       | %d                                       |
| unsigned short                                              | 2                        | 0 to 65,535                             | %d                                       |
| unsigned short int                                          | 2                        | 0 to 65,535                             | %hu                                      |
| long long int                                               | 8                        | -9 quintillion to 9 quintillion         | %lld                                     |
| unsigned long long int                                      | 8                        | 0 to 18 quintillion                     | %llu                                     |
> When the data stored is more than the range, then **overflow** will occur.

> long int and int are the same.

> By default, “char” datatype is an “signed char”.

> When a datatype is unsigned, it will take the negative numbers range as positive and add it.