Status:
Tags:
Links: [[A Instruction (CPU)]]
___
# C Instruction (CPU)
## Chart
![[c instruction visual.png]]
## Notes
Performs a compution on a certain destination
- comp is a logical/arithmetic computation
	![[comp examples.png|600]]
- dest refers to RAM[A]
	- null, M, D, MD, A, AM, AD, AMD
- jump is flow control
	- null, JGT, JEQ, JGE, JLT, JNE, JLE, JMP
Semantics:
- Computes value of comp and stores it in dest
- If the jump is true, it exectures the instruction stored in ROM[A]
Examples:
```
//Set RAM[300] to value of D register - 1
@300 //A = 300
M = D-1 //RAM[300] = D-1

// If (D-1==0) jump to execute the instruction stored in ROM[56]
@56 //A = 56
D-1;JEQ //if (D-1==0), goto 56
```

___
References: