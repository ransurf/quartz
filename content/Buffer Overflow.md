Status: 
Tags: 
Links: [[Buffer Overflow]]
___

# Buffer Overflow
## Principles
?
- If function does not perform bound-check when writing to array, overflowing it
	- bound check is if size <= array size

Buffer  flow can lead to
?
- corruption of stack data
	- Values (local vars, registers)
	- Return address
	- Stack smashing
- Vulnerable to attacks
	- Code injection
___
References:

Created:: 2022-03-14 03:07
