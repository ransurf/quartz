---
title: Computer Memory
---
Status: 
Tags: #295/cpu/memory
Links: [Central Processing Unit (CPU)](out/central-processing-unit-cpu.md)
___
# Computer Memory
## Principles
### Storage
- Linear array of bytes
- Smallest adressable is 1 byte / 8 bits
	- Each byte has unique adress, byte-adressable
- CPU reads a word a time
[![Image from Gyazo](https://i.gyazo.com/07c68637b877d38cdfe17bd9e412de0f.png)](https://gyazo.com/07c68637b877d38cdfe17bd9e412de0f)
### Segments
- [Memory Stack](out/memory-stack.md)
	- Runtime stack, local variables
- Heap
	- Dynamically allocated as needed
		- Explicitly released malloc(), free(), delete, etc
- Data
	- Statically allocated data
		- *ex) global vars, static vars, string consts*
- Text
	- Executable machine instructions
		- Read-only
- Shared libraries
	- Executable machine instructions
	- Read only
#### Example
Where would each part of the code go?
[![Image from Gyazo](https://i.gyazo.com/d6f1cf98775cbe98b7404047b28625c5.png)](https://gyazo.com/d6f1cf98775cbe98b7404047b28625c5)
?
[![Image from Gyazo](https://i.gyazo.com/9023be27d0dd242a35d11c0f0b8b66c1.png)](https://gyazo.com/9023be27d0dd242a35d11c0f0b8b66c1)
___
References:

Created:: 2022-02-12 15:55
