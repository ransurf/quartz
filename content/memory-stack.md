---
title: Memory Stack
---
Status: 
Tags: 
Links: [Computer Memory](out/computer-memory.md)
___

# Memory Stack
## Principles
- [Hand Tracing Stack](out/hand-tracing-stack.md)
### [x86-64 Assembly](out/x86-64-assembly.md) 
[![Image from Gyazo](https://i.gyazo.com/fe35a410af969866615f1d42e159b917.png)](https://gyazo.com/fe35a410af969866615f1d42e159b917)
- initially empty
- has stack-specific instructions and register
#### %rsp
- points to address of last used byte on stack
- initialized to "top of stack" at startup
- stack grows towards low memory address
- Should always go back to original position after end of function
#### push* src
- `src` can be
	- imm
	- register
	- memory
- execution
	1. get value of operand src
	2. decrement %rsp by 8 as you need to go down the stack
	3. store value at (memory adress stored in) %rsp
- `%rsp` is an implicit register
#### pop* dest
- `dest` can be
	- register
- execution
	1. read value at (memory adress stored in) %rsp and load this value in operand dest
	2. increment %rsp by 8
- `%rsp` is implicit register
[![Image from Gyazo](https://i.gyazo.com/8da829446fbca68b255f4c819e797ca7.png)](https://gyazo.com/8da829446fbca68b255f4c819e797ca7)
#### Uses
Store local variables
Steps:
- Setup code to create space on stack
	- `subq $16, %rsp`
- Spill onto stack
	- `movq %rax, 8(%rsp)
- Clean-up code (restore stack)
	- `addq $16 %rsp`
___
References:

Created:: 2022-02-12 16:11
