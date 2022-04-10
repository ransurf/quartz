---
title: HACK CPU
---
Status:
Tags:
Links: [Nand2Tetris Unit 5](out/nand2tetris-unit-5.md)
___
# HACK CPU
- Part of the [HACK Computer](out/hack-computer.md)
- [HACK CPU Implementation](out/hack-cpu-implementation.md)
## Diagram
### Abstract
![hack cpu diagram.png](None)
### Intricate
![hack cpu implementation.png](None)
## Properties
- 16-bit processor
- Can execute current instructions, and finds out what instruction to execute next
- [HACK CPU Instruction Handling](out/hack-cpu-instruction-handling.md)
- [HACK CPU Execution](out/hack-cpu-execution.md)
## Inputs
- Data value
- Instruction
- Reset bit
## Outputs
- writeM
	- Used as address for memory
- outM
	- Goes into memory 
- addressM
	- Goes into memory 
- pc
	- Goes back into ROM to find next instruction input
___
References: