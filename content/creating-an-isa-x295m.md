---
title: Creating an ISA (x295M)
---
Status: 
Tags: 
Links: [Instruction Set Architecture (ISA)](out/instruction-set-architecture-isa.md)
___

# Creating an ISA (x295M)
## Principles
> Example is x295M

### Registers and memory model
?
- Number of registers
	- 0
- Each memory adress bit count
	- m = 32
- Word size = 32 bits
- Byte-adressable memory ?
	- Implies n = 1 byte
- Memory size = 2^m x n

### Set of instructions
Add, Sub, Mul
General format
`{Opcode (2)} {dest (30)} {00} {src1(30)} {00} {src2(30)}`
- Each pair of 2 bits + var is 32 bits = 1 word

Follows design guideline since:
- Few as possible created
	- 1 format
- Formats are same length
	- 3 x 32 bits
- Same purpose in same location
	- Only 1 format so yes

### Assembly to Machine
- Keep in mind how the operands are stored as assembly might be different from machine
___
References:

Created:: 2022-03-21 20:13
