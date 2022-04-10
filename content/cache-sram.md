---
title: Cache (SRAM)
---
Status: 
Tags: #cards/cmpt295/mp 
Links: [Microprocessor](out/microprocessor.md)
___

# Cache (SRAM)
## Principles
?
- Cache holds a subset of main memory, and is mediator between [Microprocessor](out/microprocessor.md) and [RAM](out/ram.md)

- Each line can hold a copy of 64 bytes from main memory

How it works
?
- Example: `Load a, RC`
- Microprocessor reads from cache
- If line requested in cache, data is served (cache hit)
	- a is sent to mp
- If line requested is not in cache, cache must load from main memory (cache miss)
	- a is read from the next level down, repeats until found

___
References:

Created:: 2022-04-08 02:58
