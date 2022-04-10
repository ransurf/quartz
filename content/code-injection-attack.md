---
title: Code Injection Attack
---
Status: 
Tags: #cards/cmpt295/assembly/stack
Links: [Memory Stack](out/memory-stack.md)
___

# Code Injection Attack
## Principles
Can happen by
?
- Inputting string that contains malicious executable code
- Higher in the stack there might be a return address that will be called, but the malicious string will replace it and be run instead
<!--SR:!2022-03-24,3,130-->

## Solutions

Properly copying strings
?
- strcpy copies as much as possible without regard to size
- strncpy stops at n
- strlcpy stops at n-1 characters, allowing for `\0` null character in the stored space
<!--SR:!2022-03-24,3,130-->

Random stack buffers
?
- Shifts initial `%rsp` address for stack
	- Different every run, makes it more complicated to determine where things are stored
<!--SR:!2022-03-24,3,130-->

- Mark stack segment as non-executable
- Stack [Canary Value](out/canary-value.md)

Control flow enforcement technology
___
References:

Created:: 2022-03-14 03:14
