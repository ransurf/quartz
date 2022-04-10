---
title: x86-64 Assembly
---
Status: 
Tags: #cards/cmpt295/assembly 
Links: [Coding MOC](out/coding-moc.md)
___
# x86-64 Assembly
## Principles
### Data
- 16 integer registers of 64 bits each: can manipulate either 1, 2, 4 or 8 bytes (memory 
address of 8 bytes as well) depending on the register name used
- Floating point registers of 64 bits each: can manipulate either 4 or 8 bytes 
depending on the register name used
 - No aggregate types such as arrays or structures

Data management
- [Caller vs Callee](out/caller-vs-callee.md#Registers)
### Operations
1. Memory referenence => data transfer instructions
	- Transfer data from memory to register using [mov*](None)
		- Load (mem -> reg)
		- Store (reg -> mem)
		- Move (reg -> reg)
1. Arithmetic and logical => data manipulation instructions
	- Perform calculations
		- *ex) Arithmetic, logic, shift*
1. Branch and jump => program control instructions
	- Transfer control
	- Unconditional jumps to/from functions
	- Unconditional/conditional branches
### Syntax
- always include `.global {file_name}` in top
- functions look like
```
func_name:
# do something
```

- `$` is used for immediate/fixed value
- `%` is used for referencing register
- Putting () automatically refers to adress
	- Don't use it for non-memory adresses
- mov*



Function calls ;; call and ret
<!--SR:!2022-03-29,8,150-->
### Parameters
![Assembly.png](None)

### Operands
- [Load Effective Address (leaq)](out/load-effective-address-leaq.md)
- [Memory adressing modes](out/memory-adressing-modes.md)
### Insructions
- [One Operand Arithmetic Instructions](out/one-operand-arithmetic-instructions.md)
- [Two Operand Arithmetic Instructions](out/two-operand-arithmetic-instructions.md)
- [Two Operand Logical Instructions](out/two-operand-logical-instructions.md)
- [Two Operand Shift Instructions](out/two-operand-shift-instructions.md)

testq ;; param & param
<!--SR:!2022-03-22,1,144-->

Operation sizes
movb size of data transfer ;; 1 byte
<!--SR:!2022-03-28,7,170-->
movw size of data transfer ;; 2 bytes
<!--SR:!2022-03-29,8,174-->
movl size of data transfer ;; 4 bytes
<!--SR:!2022-03-26,5,150-->
movq size of data transfer ;; 8 bytes
<!--SR:!2022-03-29,8,174-->

mov src, dest
?
- copies variable info into a new one
<!--SR:!2022-03-25,4,154-->

cmov src, dest
?
- cmov is used to accompany cmp
	- if cmpl, then cmov
- Not to be used in expensive, risky, or side effect computations
<!--SR:!2022-03-24,3,134-->

#### call
syntax: `call func` where `func` -> label (memory adress of first instruction of callee - function being called)
program counter: generic term that specifies next adress of instruction, denoted as `%rip` (register instruction pointer)
- stored in [Memory Stack](out/memory-stack.md)

- when call executes:
	1. save value of program counter (PC -> %rip) on stack
		- pushq %rip
			- return address, memory address of instruction after call func instruction
	1. set program counter (PC -> %rip) to memory address of first instruction of func
		- `movq "func, %rip`
	2. Start executing func
		- `jmp func`

#### ret
syntax: ret

- execution
	1. load return address from stack onto %rip
		- popq %rip
	1. jump to return address (of caller) and start executing the instruction at that memory address
		- `jmp %rip`
##### Example
[Caller vs Callee](out/caller-vs-callee.md) and [](None#ret)
###### multstore

Applies multiplication then stores value into dest
```c
void multstore(long x, long y, long *dest) {
	long t = mult2(x, y);
	*dest = t;
	return;
}
```
multstore in assembly
```
0000000000400540 <multstore>:
400540: push %rbx # Save %rbx
400541: mov %rdx,%rbx # Save dest
400544: callq 400550 <mult2> # mult2(x,y)
400549: mov %rax,(%rbx) # Save at dest
40054c: pop %rbx # Restore %rbx
40054d: retq # Return
```
Multiplies 2 numbers
```c
long mult2(long a, long b) {
	long s = a * b;
	return s;
}
```
mult2 in assembly
```
0000000000400550 <mult2>:
400550: mov %rdi,%rax # a
400553: imul %rsi,%rax # a * b
400557: retq # Return
```
### Procedures
- [Assembly Loops](out/assembly-loops.md)
- [Converting C code to Assembly](out/converting-c-code-to-assembly.md)
___
# Backlinks
```dataview
list from [x86-64 Assembly](out/x86-64-assembly.md) AND !outgoing([x86-64 Assembly](out/x86-64-assembly.md))
```
___
References:

Created:: 2022-01-31 14:47