---
aliases:
---
Status:
Tags:
Links: [[) CMPT 295 - Introduction to Computer Systems]]
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
- [[Binary rounding rules]]

### 19
- [[Memory Stack#Uses]]
- [[Caller vs Callee#Registers]]
- [ ] Example to try

### 20
- [[Recursion#x86-64 Assembly]]
- [ ] Example to try

### 22
- [[Buffer Overflow]]
- [[Canary Value]]
- [[Code Injection Attack]]

### 23
- [[Floating Point Data]]
- [[Microprocessor]]
- [[Instruction Set Architecture (ISA)]]

### 24
[[MIPS]]

### 26
- [[Creating an ISA (x295M)]]

### 29
- [[Microprocessor Sequential Execution]]

### 30
- [[Clock register]]
- [[Microprocessor Staged Execution]]

### 31
- [[Microprocessor Pipeline Execution]]

### 33
- [[Code Optimization]]

### 35
- [[Microprocessor Superscalar Execution]]

### 36
- [[Locality]]

___
References:

Created:: 2022-03-03 20:43
