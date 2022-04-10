Status: 
Tags: 
Links: [[) CMPT 295 - Introduction to Computer Systems]]
___
# CMPT 295 Course Outline
[![Image from Gyazo](https://i.gyazo.com/eca78ba1f32101e95fbdc6d758e28538.png)](https://gyazo.com/eca78ba1f32101e95fbdc6d758e28538)
- [[Von Neumann Architecture]]
- [[Data Representation]]
- Shannon's master thesis
	- Claude Shannon applied boolean algebra onto design and anlysis of digital systems/circuits

## Machine Level Programming
- [[x86-64 Assembly]]
- [[Central Processing Unit (CPU)]]
- [[Caller vs Callee]]
- [[]]
### Makefile Syntax
- gcc -E main.c > main.i
	- implements include files into program
	- E
	- S is assembly
	- g allows to use debugger
	- Wall is show all warnings
	- c converts assembly to object file
	- o is executable
	- ss some store
### Questions
How does c program become stored in memory?
- Loader

How is c program executed by microprocessor?
- [[Converting C code to Assembly]]

- First it looks at `%rip` to see what instruction needs to be called
- Run function, then increment PC
- Have visuals for each register to help with hand tracing


Steps of call instruction
- When callq, add return address (%rip) to stack to return later
- %rip is set to callq, runs the new called function

- When coming across a ret, it grabs from stack and puts into %rip
- When calling a function inside a function, its return value will be stored in %rax
___
# Backlinks
```dataview
list from [[CMPT 295 Course Outline]] AND !outgoing([[CMPT 295 Course Outline]])
```
___
References:

Created:: 2022-01-10 14:42
