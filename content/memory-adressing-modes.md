---
title: Memory adressing modes
aliases:
---
Status:
Tags: #cards/cmpt295/assembly
Links: [x86-64 Assembly](out/x86-64-assembly.md)
___

# Memory adressing modes

## Principles
Help specify instruction operands

Use cases for `q` type
?
- Push/pop
- Adding displacement to address
<!--SR:!2022-03-22,1,135-->

Use cases for `l` type
?
- Moving values to registers
<!--SR:!2022-03-23,2,155-->

Use cases for `b` type
- Adding integers

Dereferencing is for
?
- Getting the adress
<!--SR:!2022-03-23,2,155-->

### Variables
Immediate
- Constant int used as operand in instruction
- Operand syntax: Imm
- *ex) movq $0x4 %rax, movb $-17. %al*

Register
- used as operand in instruction
- Operand value: R[$r_a$]
- Operand syntax: %$r_a$
- *ex) movq, %rax, %rdx*

Memory adressing mode (expression) used as operand in an instruction

### Types
?
- Absolute
- Indirect
- "Base + displacement"
- 2 indexed
- 4 scaled indexed
<!--SR:!2022-03-26,5,150-->

#### Absolute memory adressing mode
?
- Use memory adress as operand directly in instruction
	- Operand called `immediate`
- Operand syntax: `Imm`
- Effect: `M[Imm]`
- *ex) call plus* where plus is a function
<!--SR:!2022-04-07,21,130-->

#### Indirect memory adressing mode
?
- When a register contains an adress
	- Similar to pointer in C
- To access, use parentheses
	- *ex) ($r_b$)*
		- b is base,
- Effect: M[R[$r_b$]]
	- R is register
<!--SR:!2022-03-25,4,130-->

#### "Base + displacement" memory adressing mode
?
- General syntax: Imm($r_b$)
	- Call adress, then add value
		- Base is adress, displacement is value
- Effect: M[Imm + R[$r_b$]]
- *ex)movq %rax, -8(%rsp)*
	- leaq 7(%rdi), %rax
	- Why 8? alignment, make space onto stack
<!--SR:!2022-04-04,18,130-->

#### Indexed memory adressing mode
?
- Adding offset to a base adresss
	- Help visit every value
	- ideal to store and access values stored in arrays
- **General syntax 1:** ($r_b$, $r_1$)
	- Effect: M[R[$r_b$] + R[$r_i$]]
	- Example: movb (%rdi, %rcx), %al
	- r_i is an iteration index
- **General syntax 2:** Imm($r_b$, $r_i$)
	- Effect: M[Imm + R[$r_b$] + R[$r_i$]]
	- Example: movw 0xA(%rdi, %rcx), %r11w
<!--SR:!2022-03-27,6,150-->

#### Scaled indexed memory adressing mode
?
- s can only be 1,2,4,8
1. **General Syntax:** (, $r_i$, s)
	- Effect: M[R[$r_i$] * s]
	- *ex) (, %rdi, 2)*
2. **General Syntax:** Imm(,$r_i$, s)
	- Effect: M[Imm + R[$r_i$] * s]
	- *ex) 3(, %rcx, 8)*
3. **General Syntax:** ($r_b$, $r_i$, s)
	- Effect: M[R[$r_b$] + R[$r_i$] * s]
	- *ex) (%rdi, %rsi, 4)*
4. **General Syntax:** Imm($r_b$, $r_i$, s)
	- Effect: M[Imm + R[$r_b$] + R[$r_i$] * s]
	- *ex) 8(%rdi, %rsi, 4)*
- Leaq's effect is to not reference any memory !!!
<!--SR:!2022-03-30,9,150-->

### Example
___

# Backlinks
```dataview
list from [Memory adressing modes](out/memory-adressing-modes.md) AND !outgoing([Memory adressing modes](out/memory-adressing-modes.md))
```
___
References:

Created:: 2022-02-04 12:50
