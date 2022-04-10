---
title: CMPT 295 Lectures
aliases:
---
Status:
Tags:
Links: [) CMPT 295 - Introduction to Computer Systems](out/-cmpt-295-introduction-to-computer-systems.md)
___

# CMPT 295 Lectures

## Principles

### 4 - Data Representation, Integer Arithmetic
- Data overflow from adding, truncation
- Unsigned int
	- True sum is without overflow, actual is when considering overflow
- Signed int
	- Becomes negative since the last digit is stored as negative
	- Discarding carry out is same as modular arithmetic
	- If you know true sum and want to find actual, subtract $2^w$
	- If negative + positive, then true sum = actual sum
- Carry out is the extra number not fit into memoryz
- Subtraction is addition but with a negativve number

Multiplication
- needs 2x the capacity of the valuesz

- [ ] unsigned and signed addition formulas for true and actual sums

### 5 - Upsizing
- When you upsize, you add 0's to left
- If int and short have same value and you compare, short will be upgraded to an int
	- ui > us is true since ui = xbeef0000 and us = 0000beef
	- if signed though, then ui < us since ui msb turns ui negative
		- us gets padded with 1'sdddz
- turning unsigned to signed pads left with 1's

### 6
- Scientific vs normalization

Normalization
?
- Move decimal until left-most 1 is on the left of it
- Exponent is number moved

Why add 1 to fracz

### 7
- [Binary rounding rules](out/binary-rounding-rules.md)

### 19
- [Memory Stack](out/memory-stack.md#Uses)
- [Caller vs Callee](out/caller-vs-callee.md#Registers)
- [ ] Example to try

### 20
- [Recursion](out/recursion.md#x86-64 Assembly)
- [ ] Example to try

### 22
- [Buffer Overflow](out/buffer-overflow.md)
- [Canary Value](out/canary-value.md)
- [Code Injection Attack](out/code-injection-attack.md)

### 23
- [Floating Point Data](out/floating-point-data.md)
- [Microprocessor](out/microprocessor.md)
- [Instruction Set Architecture (ISA)](out/instruction-set-architecture-isa.md)

### 24
[MIPS](out/mips.md)

### 26
- [Creating an ISA (x295M)](out/creating-an-isa-x295m.md)

### 29
- [Microprocessor Sequential Execution](out/microprocessor-sequential-execution.md)

### 30
- [Clock register](out/clock-register.md)
- [Microprocessor Staged Execution](out/microprocessor-staged-execution.md)

### 31
- [Microprocessor Pipeline Execution](out/microprocessor-pipeline-execution.md)

### 33
- [Code Optimization](out/code-optimization.md)

### 35
- [Microprocessor Superscalar Execution](out/microprocessor-superscalar-execution.md)

### 36
- [Locality](out/locality.md)

___
References:

Created:: 2022-03-03 20:43
