---
title: Data Memory
---
Status:
Tags:
Links: [Nand2Tetris Unit 3](out/nand2tetris-unit-3.md)
___
# Data Memory
Part of the [HACK Computer](out/hack-computer.md)
## Principles
Worth vs value of a bit
?
- Worth is the potential, what it represents, while value is the current value in relation to worth

Memory models (addressable)
?
- Word (only start of each register)
	- Texas instruments
- Memory size (can access any byte)
	- AMD chips
### Types
- Main memory [RAM](out/ram.md)
- Secondary memory (disks)
- Volatile (RAM) / Non-Volatile (Disks)

- Why only 0 and 1 in memory cell?
	- Voltage levels transmitted on noisy wires determine what number based on range
		- ex) 0.0 -> 0.2v = 0, 0.9 -> 1.1v = 1

- The width is the amount of data in a single register, and the adress is the location of a register within a larger chip

### Ordering
- Most significant byte is left hand side as it dictates larger digit
- Least significant byte is right hand side as it represents smaller number
- Little endian
	- start at higher address and work down
	- Little *end* as it finishes reading at the lower address
- Big endian
	- Start at lower address and work up


- Left shift
	- x << y
	- Shift bit vector x left y position
	- Fill right with 0
- Right shift
	- x >> y
	- Shift bit x right y positions
		- Logical shift, fill left with 0
		- Arithmetic shift, move lsb to msb

## Tiers
[![Image from Gyazo](https://i.gyazo.com/fa50b7ac330e20bf93d96873cc3a4800.png)](https://gyazo.com/fa50b7ac330e20bf93d96873cc3a4800)
___
References: