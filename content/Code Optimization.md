---
aliases:
---
Status:
Tags: #cards/cmpt295/compilers
Links: [[Coding MOC]]
___

# Code Optimization

## Principles
gcc has different forms of optimization: `-Og` `-O1` `-O2`

Code optimization helps with:

### Reduction in Strength
?
Turn existing code into a less demanding operation

Example
- y = x / 2.0 => y = x * 0.5
- Division is more expensive than multiplication
	- Easy to do if constant

### Remove unecessary function call
?
For a function that adds 1,2,...,7:
- Og reduces bloat
- O1 just calculates and automatically includes it

### Code Motion (-O1)
?
- Moving code
	- Instead of calculating N*i in a loop multiple times, calculate it beforehand

## Limitations
- Optimization blockers
	- Function calls, can't tell if there is side effect
- Memory aliasing
	- May not be able to determine when pointers are aliased

## Solutions
- Reduction in strength
- Code and function calls motion
- Memory references in loops: use local var instead
- Branching minimization
	- Try to not have to use if statements
- Inline subsittution
	- Replace func calls with func implementation

### For Instruction-level parallelism
- Be careful of using too many registers

#### Loop unrolling (kxc)
?
- Restructure code to allow multiple arith calculations in parallel due to multiple units, leading in less loop iterations
	- ex) Increment for loop by 2 each time, add A[i] and A[i+1] to total
	- Denoted by k being how much you unrolled

Re-associating (denoted as a)
?
- [![Image from Gyazo](https://i.gyazo.com/389cc0b860b2acfa053e2d9a34cf1d60.png)](https://gyazo.com/389cc0b860b2acfa053e2d9a34cf1d60)
- Each horizontal level is a clock cycle
- total = total + (A[i] + A[i+1])
- Slowly converges to 1 clock cycle per iteration

Accumulating 
?
- denoted as c where b is how many accumulators you are using in your code

___
References:

Created:: 2022-04-07 01:01
