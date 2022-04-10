Status: 
Tags: 
Links: [[CMPT 295 Course Outline]]
___
# Converting C code to Assembly
## Principles
- If you need to manipulate a variable but it still needs to be used in a future computation, create a temp variable
### Converting C to Machine
- fetch next instruction from memory into CPU
- update the program counter
- decode the instruction
- execute the instruction

## Examples
```c
long arith(long x, long y, long z) {
  long t1 = x + y;
  long t2 = z + t1;
  long t3 = x + 4;
  long t4 = y * 48;
  long t5 = t3 + t4;
  long rval = t2 * t5;
  return rval;
}
```
```assembly
# Filename: arith.s
# Description: Demo of arithmetic and logical 
# Auhtor: AL


# long arith(long x, long y, long z) {
#   long t1 = x + y;
#   long t2 = z + t1;
#   long t3 = x + 4;
#   long t4 = y * 48;
#   long t5 = t3 + t4;
#   long rval = t2 * t5;
#   return rval;
#  }

	.globl	arith
arith:  # mine
     # x -> %rdi, y -> %rsi, z -> %rdx
     # addq %rsi, %rdi # Bad! because overwrites %rdi which is needed later on for "t3 = x + 4"
     # addq %rdi, %rsi # Bad! because overwrites %rsi which is needed later on for "t4 = y * 48"
     movq %rdi, %rax # x -> %rax <- function's returned value
     addq %rsi, %rax # t1 = x + y; t1 -> %rax
     addq %rdx, %rax # t2 = z + t1; t2 -> %rax
     addq $4, %rdi   # t3 = x + 4; t3 -> %rdi
     imul $48, %rsi  # t4 = y * 48; t4 -> %rsi
     addq %rsi, %rdi # t5 = t3 + t4; t5 -> %rdi
     imul %rdi, %rax # rval = t2 * t5; rval -> %rax
     ret
```
___
# Backlinks
```dataview
list from [[Converting C code to Assembly]] AND !outgoing([[Converting C code to Assembly]])
```
___
References:

Created:: 2022-02-05 20:38
