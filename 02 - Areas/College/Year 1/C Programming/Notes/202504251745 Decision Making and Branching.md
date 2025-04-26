---
date: 2025-04-25T17:45
tags:
  - C
cssclasses:
  - center-titles
  - page-manila
---
# DECISION MAKING AND BRANCHING

## if/else Statements

They are used to add choices in a program.

To use `if` and `else` statement, type this:
```c
if(age <= 18){
printf("YOU ARE A MINOR!");
}
else if(age == 18){ // Just like elif in python
printf("You are 18 years old.");
}
else{
printf("You are old.");
}
```

## switch Statements

A `switch()` statement is a more efficient alternative to many `else if` statements.

Example:
```c
// Instead of typing
else if(marks > 33){
printf("You passed!");
}
else if(marks < 33){
printf("You failed!");
}

// Type this
switch(grade){ // Instead of marks, the user types the Grade
	case 'A': // If the user types A, it will print you passed!
		printf("You passed!");
		break;
	case 'F': // If the user types F, it will print you failed!
		printf("You failed!");
		break;
	default:
		printf("Not a valid grade");
}
```

> A `switch` keeps on running until it encounters a `case` having `break` statement in it.

> A `switch` statements only tests for equality.

> It is necessary to type `break` in the `case` statements, as it helps in exiting the loop. If no `break` are added then it will print all the outputs in all statements, which in the above case it will print “You passed!” and “You failed!” at the same time.