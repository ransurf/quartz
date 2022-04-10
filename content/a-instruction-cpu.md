---
title: A Instruction (CPU)
---
Status:
Tags:
Links: [HACK Computer](out/hack-computer.md) - [C Instruction (CPU)](out/c-instruction-cpu.md)
___
# A Instruction (CPU)
Symbolic Syntax: 
- @value
	- value is either:
		- a non-negative decimal constant
		- a symbol referring to such a constant
Binary Syntax:
`0value` where value is a 15-bit binary number
- a 1 before the value would be a [C Instruction (CPU)](out/c-instruction-cpu.md)
Semantics:
- Sets A register to value
- RAM[A] becomes selected register
	- ex) @21 sets the a register to 21, and RAM[21] becomes the selected RAM register
		- can now set RAM[A] by setting M=value
___
References: