---
title: HACK Computer
---
Status:
Tags:
Links: [Nand2Tetris Unit 4](out/nand2tetris-unit-4.md)
___
# HACK Computer
- Computer built in Nand2Tetris course
- [HACK Computer Implementation](out/hack-computer-implementation.md)
## Diagram
![hack computer diagram.png](None)
## Parts
- [Reset Button](out/reset-button.md)
- [Data Memory](out/data-memory.md) (RAM)
- [Instruction Memory](out/instruction-memory.md) (ROM)
- [HACK CPU](out/hack-cpu.md) (performs instructions)
	- 3 registers in CPU:
		- D (16-bit value)
		- [A Instruction (CPU)](out/a-instruction-cpu.md) (16-bit value)
		- M (16-bit register adressed by A)
## Characteristics
- 16-bit machine
- Instruction bus, data bus, address bus
	- Highways???
- Can use [Binary](out/binary.md) or symbolic language
	- Refer to [HACK Programming](out/hack-programming.md)
## Processes
### Running a Program
1. Load the program into the ROM
2. Press reset
3. Tada
___
References: