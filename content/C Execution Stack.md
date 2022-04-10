Status: 
Tags: 
Links: [[C MOC]]
___
# C Execution Stack
- Data structure that stores the information about the functions called during the execution of a program.
	- Local variables are stored on the stack, deleted when function ends

### Fields
For each function the stack stores the following information:
- Parameters of the function
- local variables
- return values
- return address → when a function completes, it returns control to the function that called i.

Dynamically allocated memory are stored on the heap
- [[C Memory Allocation|malloc]] vars don't die

Data structure with two principal operations
`push(elem)` adds element to collection
`pop()` removes most recently added from the collection
- ex) A stack of blocks
___
# Backlinks
```dataview
list from [[C Execution Stack]] AND !outgoing([[C Execution Stack]])
```
___
References:

Created:: 2021-09-27 16:17
