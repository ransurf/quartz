---
title: C Pointers and References
---
Status: 
Tags: 
Links: [C MOC](out/c-moc.md)
___
# Pointers and References
- [C Constant Pointers](out/c-constant-pointers.md)
- [Void Pointers](out/void-pointers.md)
## Pointers
- Dereferencing
	- useful when you only have the address in memory and you want to read or write the value in the address.
- 8 bytes
- Hold the location of variables
- Can change parameters of functions
- Used to modify variables sent to a function by getting adress as parameter
	- `void foo(int* a)` as parameter, call using `foo(&a)`
-   `*` plays 2 roles
    -   When we declare a variable which is a pointer.
    -   When we want the value in the address. (Read or write)
### Uses
- Allow us the modify parameters in a function
- Allows us to pass large objects to a function with a single pointer.
- Optimization: Avoids duplicating data
- Arrays are implemented using pointers in C
    -   So are strings
### Syntax
`&` to get adress of a value
`*` access value at the adress
```c
int* px = &x; //create pointer var to adr of x

*px = 7; //value at var px is changed to 7

int x = 5; int* px = &x; // pointer to location x
//int* is a type 
printf("The address in memory of %d is %p|", x, px); 
>> The address in memory of 5 is 0x9a58af3c4 
// %p is a pointer and address is usually in hexadecimal

```
## Questions
[![Image from Gyazo](https://i.gyazo.com/f52ec4e9f31fb162f2909413d481854d.png)](https://gyazo.com/f52ec4e9f31fb162f2909413d481854d)
?
a = 7, b = 1, c = 2
___
# Backlinks
```dataview
list from [C Pointers and References](out/c-pointers-and-references.md) AND !outgoing([C Pointers and References](out/c-pointers-and-references.md))
```
___
References:

Created:: 2021-09-13 14:35
