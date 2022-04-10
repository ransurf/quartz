---
title: HACK CPU Execution
---
Status:
Tags:
Links: [HACK CPU](out/hack-cpu.md)
___
# HACK CPU Execution
## Diagram
![hack cpu diagram.png](None)
## Examples
- @x is an instruction, and address change would be outputted as addressM
- If M is on the left side of the instruction (M = D-1), value is read from inM
	- Conversely, if on the right side (A  = M), ALU output is emitted by outM, and writeM bit is asserted
___
References: