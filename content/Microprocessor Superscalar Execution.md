---
aliases:
---
Status:
Tags: #cards/cmpt295/mp
Links: [[Microprocessor]]
___

# Microprocessor Superscalar Execution

## Principles
?
- Modern microprocessors have instruction level parallelism
	- Have multiple functional units, which can be assigned one instruction per clock cycle

[![Image from Gyazo](https://i.gyazo.com/3473c99c9786975ba4617db295baf3b3.png)](https://gyazo.com/3473c99c9786975ba4617db295baf3b3)
- Operation results is shared bus that goes back into register file
- Output of codes are added together and converted into proper intention of machine code

### Out of Order Execution (OoOE)
- Rearrange execution order of instructions to:
	- Avoid hazards
	- maximize use of functional units
- How:
	- Instruction Control Unit (ICU) fetches machine level instructions from memory (instruction cache)
	- Decodes and analyzes for data dependencies (hazards)
	- Avoids hazards by running eligible micro-operations by Execution Unit (EU)
		- Each clock cycle
	- Retirement Unit of ICU "puts everything back in order" to resemble sequential execution

___
References:

Created:: 2022-04-08 02:30
