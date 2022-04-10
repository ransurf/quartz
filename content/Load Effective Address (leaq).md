Status: 
Tags: #cards/cmpt295/assembly 
Links: [[x86-64 Assembly]]
___
# Load Effective Address (leaq)
## Principles
?
- Loads adress onto register
- leaq (%rax, %rcx, s), %rdx
	- add rax to rcx
	- multiply rdi by s, s is either 1,2,4,8
	- store into rdx
<!--SR:!2022-03-30,9,150-->

- `leaq 32(%rsp), %rsi` loads address to rsi
	- If storing address of a byte/short, then still use q since an address is 8 bytes
___
# Backlinks
```dataview
list from [[Load Effective Address (leaq)]] AND !outgoing([[Load Effective Address (leaq)]])
```
___
References:

Created:: 2022-02-05 20:29
