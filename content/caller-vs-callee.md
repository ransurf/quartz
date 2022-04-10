---
title: Caller vs Callee
aliases:
---
Status:
Tags: #cards/cmpt295/assembly
Links: [x86-64 Assembly](out/x86-64-assembly.md)
___

# Caller vs Callee

## Principles
When a caller calls a callee? (Control, data, memory)
?
- Control is passed to beginning of callee function
	- Once callee has executed, control is passed to...
		- caller function right after the callee function
- Data is passed to ...
	- callee function via function params
- Memory is ...
	- allocated when callee function starts executing
	- deallocated when callee function stops executing
<!--SR:!2022-03-31,10,170-->


### Registers

#### Callee Saved
?
- For local data, we can use unused registers
- Must preserve values of registers before using them, then restore before control is passed back to caller function
	- How? (ex. `%r13`)
		- `pushq %r13` (callee's responsibility)
		- do stuff in callee function
		- `popq %r13`
[![Image from Gyazo](https://i.gyazo.com/5e4e32ee8cc65d6afb7e0f85bc1a4216.png)](https://gyazo.com/5e4e32ee8cc65d6afb7e0f85bc1a4216)
<!--SR:!2022-03-27,6,150-->

List of callee saved
?
- rbx, r12, r13, r14, r15, rbp, rsp
<!--SR:!2022-03-26,5,150-->



#### Caller Saved
?
- Means that caller function must preserve values of registers before setting up callee's arguments into the appropriate registers
- call callee
- once caller has control, restore values again
[![Image from Gyazo](https://i.gyazo.com/452f08e730d0427596d32389418ae332.png)](https://gyazo.com/452f08e730d0427596d32389418ae332)
<!--SR:!2022-03-31,10,170-->

List of caller saved
?
- `%r10`, `%r11`, `%rax`
- paramsrdi, rsi, rdx, rcx, r8, r9
<!--SR:!2022-03-22,1,130-->

How to preserve `%r10`
?
- before calling callee, `pushq %r10`
- call callee
- upon return, `popq %r10`ddd
___
References:
<!--SR:!2022-03-27,6,150-->

Created:: 2022-02-12 15:51

### Stack
#### Over 6 Arguments
Procedure for when over 6 function arguments
?
- Subtract %rsp to allocate memory in stack
- `mov*` values onto stack
- `lea*` any addresses into stack if >6 or into register
- `mov*` values into stack if >6 or into register
- call function
<!--SR:!2022-03-24,3,130-->

Convert into assembly
[![Image from Gyazo](https://i.gyazo.com/f737dd1e7d91599fe21fe45182fb5d8d.png)](https://gyazo.com/f737dd1e7d91599fe21fe45182fb5d8d)
?
[![Image from Gyazo](https://i.gyazo.com/1f1b7e42005750d4514774acee57fe86.png)](https://gyazo.com/1f1b7e42005750d4514774acee57fe86)
<!--SR:!2022-03-22,1,130-->

#### Storage
Caller saved + Callee saved
?
[![Image from Gyazo](https://i.gyazo.com/0c20f3dda7280aa28560bc73b464e758.png)](https://gyazo.com/0c20f3dda7280aa28560bc73b464e758)
<!--SR:!2022-03-28,7,150-->