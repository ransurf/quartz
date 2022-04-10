---
title: HACK CPU Instruction Handling
---
Status:
Tags:
Links: [HACK CPU Instruction Handling](out/hack-cpu-instruction-handling.md)
___
# HACK CPU Instruction Handling
## A Instruction
- Refer to [A Instruction (CPU)](out/a-instruction-cpu.md)
### Diagram
![a instruction handling.png](None)
### Steps
1. Decodes instruction into op-code + 15-bit value
2. Stores value in a-register
3. Outputs value
## C Instruction
- Refer to [C Instruction (CPU)](out/c-instruction-cpu.md)
### Diagram
![c instruction handling.png](None)
### Steps
1. Decodes instruction into:
	1. Op-code
	2. ALU control bits
	3. Destination load bits
	4. Jump bits
___
References: