---
title: Microprocessor Staged Execution
---
Status: 
Tags: 
Links: [Microprocessor](out/microprocessor.md)
___

# Microprocessor Staged Execution
## Principles
#### Structure
- Combinational logic circuit gets cut into 5 stages
- Each stage has a pipeline register in between to save intermediate values
	- Invisible to us unlike PC
#### Diagram
- [![Image from Gyazo](https://i.gyazo.com/d525d228ce62eab3e851412e08f463e5.png)](https://gyazo.com/d525d228ce62eab3e851412e08f463e5)
- Different sections
- Imagine pipeline registers in between
#### Stages (FDEMW)
- Fetch
	- Read instruction located at memory address in PC into instruction register
- Decode
	- Decode instruction and read content of register operands (or implicit stack pointer register) from register file
- Execute
	- Perform operation using ALU unit according to opcode, inc/dec rsp, compute effective address, set condition codes
- Memory
	- Read/write data values from/to memory (memory-access instructions)
- Write back
	- Write values from/to memory (memory-access instructions)
#### Example
##### Instruction
[![Image from Gyazo](https://i.gyazo.com/17789906c32c24f8dec89fe8588c5ba3.png)](https://gyazo.com/17789906c32c24f8dec89fe8588c5ba3)
##### Process
[![Image from Gyazo](https://i.gyazo.com/709d1085ee0f513944816bd71afba738.png)](https://gyazo.com/709d1085ee0f513944816bd71afba738)

#### Analysis
[![Image from Gyazo](https://i.gyazo.com/1f7f7949c22e5106a7060f3b0a5ea9cf.png)](https://gyazo.com/1f7f7949c22e5106a7060f3b0a5ea9cf)
Minimum clock cycle
- 80ps + 20s = 100ps

Latency
- 5(80) + 5(20) = 500ps

Throughput
- 1/500

Cycles per instruction (CPI)
- 5

___
References:

Created:: 2022-04-03 17:17
