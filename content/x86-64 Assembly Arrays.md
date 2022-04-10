Status: 
Tags: #cards/cmpt295/assembly 
Links: [[x86-64 Assembly]] - [[Arrays]]
___

# x86-64 Assembly Arrays
## Principles
### 1D Arrays
?
*Remember differences of array cells differ by size of data, not just 1!*
- No arrays, just access by displacement of main pointer
- `A[i] => A + i * L
	- `A` is base memory/address of first point
	- `i` is index of array
	- `L` is sizeof(T)
<!--SR:!2022-03-23,2,150-->

Accessing memory address
?
- these operations give you the same memory address: `x + 1`, `&x[1]`
<!--SR:!2022-03-23,2,150-->

Accessing a value
?
- these operations give you the same value: `x[4]`, `*(x+4)`   
<!--SR:!2022-03-22,1,130-->

Allow for quick indexing with memory address indexing via `movq (%array start, index, char size), %register you want to save to`

How to only let loop iterate while i\<n 
?
```
# i in %ecx, N in %esi
cmpl %ecx, %esi # N - i
jle jmp endloop # N <= i
```
Adding all elements of a char array (version 1):
- Storage
	- `%rdi` contains starting address
	- `%esi` contains size (N)
	- `%ecx` contains array index
	- `%al or %ax` contains running sum
- Jump if end of array via top jmp
[![Image from Gyazo](https://i.gyazo.com/bee4a6aa850ea3308a916f643f250b77.png)](https://gyazo.com/bee4a6aa850ea3308a916f643f250b77)
<!--SR:!2022-03-22,1,130-->

Jump to end, have condition at the end to jump back if not end of array
[![Image from Gyazo](https://i.gyazo.com/3ecf2e78e688f8b6b02ccfbe3c43a701.png)](https://gyazo.com/3ecf2e78e688f8b6b02ccfbe3c43a701)

### 2D Arrays
Access row i of a 2d array
?
`A + (R * C * L)` 
<!--SR:!2022-03-22,1,130-->

Access row i col j of a 2d array
?
- `A + (i * C + j) * L` or can distribute `L`
- C is number of columns `A[R][C]`
- i is row index
- j is col ind
<!--SR:!2022-03-22,1,130-->

___
References:

Created:: 2022-03-19 04:01
