Status: 
Tags: 
Links: [[) CMPT 295 - Introduction to Computer Systems]]
___
# CMPT 295 Assignments
## 3
### Q3
p. 346
3.51! •
For a function with prototype
long decode2(long x, long y, long z);
ace generates the'tollowing assembly code:
decode2:
2 subq %rdx 1 %rsi
3 imulq %rsi, %rdi
4 movq %rsi, '/.rax
5 salq $63, %rax
6 sarq $63, %rax
7 xorq %rdi, Y.rax
8 ret
Parameters x, y, and z are passed in registers %rdi, %rsi, and %rdx. The code
stores the return value in register %rax.
Write C code for decode2 that will have an effect equivalent to the assembly
code shown
___
# Backlinks
```dataview
list from [[CMPT 295 Assignments]] AND !outgoing([[CMPT 295 Assignments]])
```
___
References:

Created:: 2022-02-06 23:58
