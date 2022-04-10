Status: 
Tags: 
Links: [[Compiling C and C++ Programs]]
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
list from [[Compiling cpp without main function]] AND !outgoing([[Compiling cpp without main function]])
```
___
References:

Created:: 2022-01-18 15:29

   

