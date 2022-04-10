Status: 
Tags: #cards/cmpt295/mp 
Links: [[Microprocessor Pipeline Execution]]
___

# Pipeline Hazards
## Principles
### Structural Hazard
?
- 2 memory access done at same time

Solution for Structural Hazard
?
- MIPS deals with this by having 2 memories:
	- Instruction memory
	- Data memory
- Read is done from one section of memory, and other is on diff side

### Data Hazard
?
- Stages are dependent on each other for data
	- Operand needed by instruction is still being computed

#### Solutions
Stalling/bubble solution
?
Stall pipeline for instruction
- Include `nop` instructions that don't require any steps so they end up being free

Data forwarding solution
?
- Forward data in pipeline to another that is currently executing or will later be into the post-register
- Target machine checks to see if value calculated is needed by a different stage

Load interlock solution
?
- Used for when `lw` and `add` instructions are sequential
- Use a bubble to stall and allow for data forwarding

Interleaving solution
?
- Move instructions around
- Instead of adding a bubble, you just move instruction

If a bubble in D, you need to stall next instructions or else there will be a multi-F moment

### Control Hazard
?
Next value of PC is unpredictable (not just PC + length of instruction)
- Occurs in call/jump (unconditional)
	- Next instruction set in D stage, where the assigned memory address is found
- Occurs in ret
	- Popped from stack
- Occurs in jump conditional
	- Can be either usual or valuae of a pipeline register

#### Solutions
- Stall pipeline (slows down mp though)
- Predict whether it will branch or not
	- can predict to always branch/jump
		- If wrong
			- Fetched code must be discarded
			- Exec continues at instruction after jump
			- Produces loss of clock cycles, lower throughput
		- If right
			- Achieve 1 instruction per clock cycle :)
___
References:

Created:: 2022-04-03 17:24
