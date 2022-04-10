---
aliases:
---
Status:
Tags: #cards/cmpt295/isa 
Links: [[Computer Architecture]]
___

# Instruction Set Architecture (ISA)

## Principles
?
- Defines the machine code (instruction set) that a [[Microprocessor]] fetches and executes, as well as the memory model
- Contains multiple [[Instruction Set]]
<!--SR:!2022-03-22,1,130-->

- [[Comparing ISAs Criteria]]

### Types
- [[MIPS]]

### Structure

#### Memory
ISA determines memory qualities like
?
- size of a word
- size and quantity of registers
- total memory size
<!--SR:!2022-03-22,1,130-->

Word size
?
- how much memory is fetched/written each cycle
	- largest size of a variable
<!--SR:!2022-03-22,1,130-->

Memory size
?
- $2^m x n$
- $2^m$ distinct addressable locations in memory with n bits each
<!--SR:!2022-03-22,1,130-->

##### Example
x86 word size ;; 64 bits
x86 addressable memory locations ;; 64
<!--SR:!2022-03-22,1,130-->
x86 bits for each addressible location in memory ;; 8
<!--SR:!2022-03-22,1,130-->
x86 has `x` int and `y` floating point registers ;; 16, 16
<!--SR:!2022-03-22,1,130-->

#### Registers
Qualities
?
- Number
- Size
- Data type
- Purpose
<!--SR:!2022-03-22,1,130-->

#### Instruction Set
- Format
- Syntax
- Description (semantic)
- Operand model: num, order, and meaning of operands
- memory adressing modes

#### Conventions
ISA is a formal specification of
?
- how control and data is passed in function calls
- how registers are preserved during function calls
	- which registered are callee or caller saved?
<!--SR:!2022-03-22,1,130-->

Example of x86 formal specifications
?
- Example: x86 has registered reserved for callee saved, return addresses, stack pointers, etc.
___
References:
<!--SR:!2022-03-22,1,130-->

Created:: 2022-03-14 03:44