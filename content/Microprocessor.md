---
aliases:
---
Status:
Tags: #cards/cmpt295/mp
Links: [[Instruction Set Architecture (ISA)]]
___

# Microprocessor

## Principles
### Implementations
- [[Microprocessor Sequential Execution]]
- [[Microprocessor Staged Execution]]
- [[Microprocessor Pipeline Execution]]
- [[Microprocessor Superscalar Execution]]

### Diagram
?
[![Image from Gyazo](https://i.gyazo.com/c1e1c9bf74b8fab55ecc54a01b2ad9b6.png)](https://gyazo.com/c1e1c9bf74b8fab55ecc54a01b2ad9b6)
- Combinational logic
	- ALU performs calculations
- Memory elements
	- Registers store data/bits for calculations
	- Clock signals through [[Clock register]]
	- If doesn't have data, then accesses [[RAM]] for new info and [[Cache (SRAM)]] 
- Bus allow data movement
- Instruction memory register holds the machine code instruction
	- [[Register File]] using register clocks
	- Each instruction fetch adds onto PC
	

### Physical Hardware
?
- Made of resistors, capacitors, diodes, and transistors
- Logic gates combine the above to perform a boolean function
	- Will be black boxes, know input/output but not implementation
	- Always active

Propogation delay
?
- $t_{pd}$
- Longest time elapsed for application of input and occurence of corresponding output

### Components
?
- [[Combinational Logic Circuits]] to manipulate bits
	- *ex) ADD*
- Memory elements to store bits (sequential logic)
- Clock signals to regulate update of memory elements

### Evaluating
Minimum Clock cycle
?
- Calculation part + register

Calculating Latency
?
- Time required to execute single instruction


Calculating Throughput
?
- Number of instructions executed per second
- GIPS
	- Number of instructions executed per second in Gigainstructions
	- sum of ps, all over


CPI
?
- Number of clock cycles per instruction

  
___
References:

Created:: 2022-03-14 03:43
