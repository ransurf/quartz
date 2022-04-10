---
title: Memory access
---
Status: 
Tags: 
Links: [Comparing ISAs Criteria](out/comparing-isas-criteria.md) - [Data Memory](out/data-memory.md)
___

# Memory access
## Principles
Most time constraining aspect of program execution
?
- due to transfer rate limitation of bus between memory and microprocessor
- Register access is faster than memory since register is inside CPU

Von Neumann bottleneck
?
- When memory is accessed during fetch stage
- During decode and execute stages
	- Value may be read or written

Calculating total memory access
?
- Calculate fetch + decode/execute

### Fetch
?
- Based on the length of each instruction
	- If an instruction is worth 3 words, then 3 fetches

### Decode/Execute
?
- Decode for each variable used
- Execute to store


## Examples
How many memory accesses
[![Image from Gyazo](https://i.gyazo.com/d7566e03c23833deed57c069323b7758.png)](https://gyazo.com/d7566e03c23833deed57c069323b7758)
?
[![Image from Gyazo](https://i.gyazo.com/829aa8e6891bb2125a6ed1e2f6ac82b0.png)](https://gyazo.com/829aa8e6891bb2125a6ed1e2f6ac82b0)

How many memory accesses
[![Image from Gyazo](https://i.gyazo.com/af822f7076a0cdb4d3d6ca29ab5772d0.png)](https://gyazo.com/af822f7076a0cdb4d3d6ca29ab5772d0)
?
[![Image from Gyazo](https://i.gyazo.com/7490552eff8c00f04731389707e7655b.png)](https://gyazo.com/7490552eff8c00f04731389707e7655b)

___
References:

Created:: 2022-03-21 20:33
