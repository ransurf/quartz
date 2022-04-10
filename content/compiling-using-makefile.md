---
title: Compiling using makefile
---
Status:
Tags: 
Links: [C MOC](out/c-moc.md)
___
# Compiling using makefile
Create using `make` in terminal
Remove makefile: `make clean`
Create makefile: `make testcirc1`

Should see something like:
```
g++ -Wall -c testcirc1.cpp
g++ -Wall -c Circle.cpp
g++ -Wall testcirc1.o Circle.o -o testcirc1
```
___
# Backlinks
```dataview
list from [Compiling using makefile](out/compiling-using-makefile.md) AND !outgoing([Compiling using makefile](out/compiling-using-makefile.md))
```
___
References: [CMPT225 Lab 1](https://www2.cs.sfu.ca/CourseCentral/225/alavergn/Labs/Lab1/1-Cpp_class.html)

Created:: 2021-09-22 14:31
