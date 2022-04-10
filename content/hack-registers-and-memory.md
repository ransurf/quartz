---
title: HACK Registers and Memory
---
Status:
Tags:
Links: [HACK Programming](out/hack-programming.md)
___
# HACK Registers and Memory
## Registers
D: Data Register
- D cannot be directly set, so we have to set D = A
	- But, D can be directly adjusted

A: Address/Data Register
- Be sure to differentiate between setting D and setting M
	- ex) @15 (D) vs @R15 (M)
M: The Currently Selected Memory Register (M=RAM[A])
## Random
- Whitespace and comments are ignored
- To prevent hackers from exploting code, it's a good idea to keep things in an infinite loop
## Symbols
- R (0..15)
- SCREEN (16384)
- KBD (24576)
## Examples of Register Manipulation
```
// D=10
@10
D=A

// D++
D=D+1

//D=RAM[17]
@17
D=M

// RAM[17]=0
@17
M=0

// RAM[17]=10
@10
D=A
@17
M=D

// RAM[5]=RAM[3]
@3
D=M
@5
M=D
___
References: