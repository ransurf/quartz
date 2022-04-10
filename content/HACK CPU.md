Status:
Tags:
Links: [[Nand2Tetris Unit 5]]
___
# HACK CPU
- Part of the [[HACK Computer]]
- [[HACK CPU Implementation]]
## Diagram
### Abstract
![[hack cpu diagram.png]]
### Intricate
![[hack cpu implementation.png]]
## Properties
- 16-bit processor
- Can execute current instructions, and finds out what instruction to execute next
- [[HACK CPU Instruction Handling]]
- [[HACK CPU Execution]]
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