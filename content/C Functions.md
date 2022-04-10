Status: 
Tags: 
Links: [[C Variables]] - [[C Syntax]]
___
# C Functions
## Function Pointers
```
int foo(char c, int n, char* s) {…}
int (*my_function_ptr)(char, int, char*);
my_function_ptr = foo;
my_function_ptr(‘A’, 10, str);
See function_pointers.c
```
___
# Backlinks
```dataview
list from [[C Functions]] AND !outgoing([[C Functions]])
```
___
References:

Created:: 2021-09-29 15:08
