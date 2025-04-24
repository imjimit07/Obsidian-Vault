---
date: 2025-04-24T23:23
tags:
  - C
cssclasses:
  - page-manila
---
# LIBRARY FUNCTIONS: INPUT, OUTPUT, MATHEMATICS, DATE AND TIME

## User Input

To accept user input, type this:
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
