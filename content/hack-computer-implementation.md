---
title: HACK Computer Implementation
---
Status:
Links: [Nand2Tetris Project 5](out/nand2tetris-project-5.md)
___
#  HACK Computer Implementation
## Notes
- Fairly easy as I just had to connect the different chips
	- Used the pins in the example for my own program
	- Super cool to see everything all build upon each other to create a computer :)

## Code
```
CHIP Computer {

    IN reset;

    PARTS:
    //RAMout
	//ROMout
	//loadRAM
	//RAMin
	//RAMaddress
	//ROMaddress
	
	CPU(inM=RAMout, instruction=ROMout, reset=reset, writeM=loadRAM, outM=RAMin, addressM=RAMaddress, pc=ROMaddress);
	Memory(in=RAMin, load=loadRAM, address=RAMaddress, out=RAMout);
	ROM32K(address=ROMaddress, out=ROMout);
}

```
## Truth Table
| time | reset | ARegister | DRegister | PC[] | RAM16K[0] | RAM16K[1] | RAM16K[2] |
| ---- | ----- | --------- | --------- | ---- | --------- | --------- | --------- |
| 0    | 0     | 0         | 0         | 0    | 0         | 0         | 0         |
| 1    | 0     | 2         | 0         | 1    | 0         | 0         | 0         |
| 2    | 0     | 2         | 2         | 2    | 0         | 0         | 0         |
| 3    | 0     | 3         | 2         | 3    | 0         | 0         | 0         |
| 4    | 0     | 3         | 5         | 4    | 0         | 0         | 0         |
| 5    | 0     | 0         | 5         | 5    | 0         | 0         | 0         |
| 6    | 0     | 0         | 5         | 6    | 5         | 0         | 0         |
| 7    | 1     | 0         | 5         | 0    | 0         | 0         | 0         |
| 8    | 0     | 2         | 5         | 1    | 0         | 0         | 0         |
| 9    | 0     | 2         | 2         | 2    | 0         | 0         | 0         |
| 10   | 0     | 3         | 2         | 3    | 0         | 0         | 0         |
| 11   | 0     | 3         | 5         | 4    | 0         | 0         | 0         |
| 12   | 0     | 0         | 5         | 5    | 0         | 0         | 0         |
| 13   | 0     | 0         | 5         | 6    | 5         | 0         | 0         |
___