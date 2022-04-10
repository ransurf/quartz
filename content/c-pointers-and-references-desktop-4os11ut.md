---
title: C Pointers and References-DESKTOP-4OS11UT
---
Status: 
Tags: 
Links: [C MOC](out/c-moc.md)
___
# Pointers and References
## Pointers
- Hold the location of variables
- Can change parameters of functions
- Used to modify variables sent to a function by getting adress as parameter
	- `void foo(int* a)` as parameter, call using `foo(&a)`
### Syntax
`&` to get adress of a value
`*` dereferencing, access value at the adress
```c
int* px = &x; //create pointer var to adr of x

*px = 7; //value at var px is changed to 7

```
___
# Backlinks
```dataview
list from [Pointers and References](None) AND !outgoing([Pointers and References](None))
```
___
References:

Created:: 2021-09-13 14:35
