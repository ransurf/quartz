---
title: Compiling cpp without main function
---
Status: 
Tags: 
Links: [Compiling C and C++ Programs](out/compiling-c-and-c-programs.md)
___
# Compiling cpp without main function
```
your_username@hostname:~$ g++ -c Circle.cpp
your_username@hostname:~$ ls C*
Circle.cpp    Circle.h      Circle.o
```

For example, you can compile testcirc.cpp using the Circle.o object file:
`g++ -o test testcirc1.cpp Circle.o`, execute using `./test`
___
# Backlinks
```dataview
list from [Compiling cpp without main function](out/compiling-cpp-without-main-function.md) AND !outgoing([Compiling cpp without main function](out/compiling-cpp-without-main-function.md))
```
___
References:

Created:: 2022-01-18 15:29

   

