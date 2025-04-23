# OVERVIEW OF C PROGRAMMING LANGUAGE

## Chapter 1

## History of Computers
- 1940's – Top Secret / Military (Used during **World War 2**)
- 1950's – Companies like IBM and DEC begin selling computers
- 1960's – More companies, less expensive, wider range of options
- Late 1960's – Various kinds of computers existed
- 1970's – Searching solution to make software (Invention of Unix)
- 1980's – Invention of **microprocessors** and PCs made them run faster
- 1990's – Making of the **Internet** (APRANET, NSFnet and WWW)
- 2000's – Amazon AWS founded in 2002 – computing as commodity

## History of C

- 1969 - B Lang - word oriented (not byte oriented)
- 1972 - C Lang - multiple types (byte and character)
- 1972-1978 - C and Unix joined to make assembly easier and be able to import to other OS's. This imporved C lang also.
- 1989 - C became popular and became standardized. Called C89/ ANSI - Void type, C++ Declarations, character sets and locales. But it was not good and difficult to use.
- 1990 - C90/ISO C (International Organization of Standards). Major revisions.
- 1999 – C99 – complex type, // comments, Unicode
- 2011 – C11 – Library improvements
- 2018 – C17 - Easier than C11
- 2023 - C23 - Latest Version

[[History of C.md]]

## Importance of C

- Most modern languages such as Python, Perl, C++, JS, etc. run on C langauage. Many of their syntax is also borrowed from C.
- Learning C can help the person understand more difficult concepts such as pointers, file handling, variables and arrays.

## Structure of a C Program
![[structure-of-c-program.png]]
```c
#include <stdio.h>
```
*#include* is a preprocessor command to include all contents in the file

This is what *stdio.h* stands for **standard input output header**. It imports various functions for input, output and file handling.

Then we write this:
```c
int main(){
    // Code
    return 0;
}
```

*main()* is the entry point of the code. the code is written procedurally (top to bottom).
At the end of the function just like Python, type *return* and then a statement. A semi-colon signifies the end of a statement.

> The function *main()* will return a 0, if the program runs succesfully with **no errors**. Otherwise, it will return **1**.

> Remember to close all statements with a semi-colon ";".

### Hello, World
To print statements in C, type this inside the *main()* function
```c
printf("Hello, World");
```
> To print in a new line, don't forget to add *\n* in the end of the sentence. Otherwise, the character will be printed on the same line without a blank space.

## Compiling a C file

To compile a C file using *gcc compiler*, type this in the command prompt
```bash
gcc Hello-World.c
```
This compiles the file and creates a *.exe* file i.e. executable. To run the executable, type this
```bash
Hello-World.exe
```

## Comments and Escape Sequences

### Comments
A comment is some text ignored by the compiler and it is used to write notes and explain code when another user is accessing the code.

To type a comment, type 2 forward slashes like this
```c
// This is a comment
```

To type multi-line comment type forward slash and an asterick and to finish type the same but in reverse like this
```c
/*
This is a multi-
line comment.
It works.
*/
```

### Escape Sequences

Escape sequences are a letter with a backslash. It is same like python.
Example:
1. `\n` - New Line.
2. `\t` - Horizontal Tab.
3. `\b` - Backspace.
4. `\f` - Formfeed page break.
5. `\v` - Vertical Tab.
5. `\\` - Backslash.
6. `\?` - Question Mark.
7. `\r` - Carrigage Return (Brings the cursor back to initial position and it doesn't print the characters before it).
8. `\bbb` - Prints the letter or value based on the **octal** code given.
9. `\xhh` - Prints the **hexadcimal** code given in the place of `hh`.

These are written inside the *printf* statement inside the quotations

To print `"`, `'`, `\` and `/` inside in the *printf* statement, type this
```c
printf("\"This is a quote.\" - Jimit Patel")
```
> Replace the symbol **after** the backslash only.