Status: 
Tags: 
Links: [[C MOC]]
___
# C User Input
-   So far we interacted with the user using `printf()`
-   We can also read the user's input using the function `scanf()`
-   The parameter to `scanf()`is a reference (address) to a variable

```c
char name[];
int age;

printf("What is your name: "); 
scanf("%s", name); &name[0];

printf("Enter your age: ");
scanf("%d", &age); // & is used to give address to write the input
```
___
# Backlinks
```dataview
list from [[C User Input]] AND !outgoing([[C User Input]])
```
___
References:

Created:: 2021-10-07 19:50
