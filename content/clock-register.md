---
title: Clock register
aliases:
---
Status:
Tags: #cards/cmpt295/mp 
Links: [Microprocessor](out/microprocessor.md)
___

# Clock register

## Principles
- Memory element
- On microprocessor
- Stores 1 bit (state)
- Synchronized with system-wide clock

### Timing Diagram
Annotated
?
[![Image from Gyazo](https://i.gyazo.com/89e1af9bb0f41d2d08e1234fdcf01ad8.png)](https://gyazo.com/89e1af9bb0f41d2d08e1234fdcf01ad8)

Things to annotate in a timing diagram
?
- Values of diagram segments
	- label 0/1
- Propagation delays
- When sampling is occuring
	- Type of sampling

Propagation delay
?
- Time between sampling and update in register value

Sampling and 3 cases
?
When the values are checked, happens when clock rises up to 1.
3 Cases:
| Load | D | Q(t+1) |
|------|---|--------|
| 0    | X | Q(t)   |
| 1    | 0 | 0      |
| 1    | 1 | 1      |


### Load Effect
?
- Loads when Clock rises up to 1

#### Load = 0
?
[![Image from Gyazo](https://i.gyazo.com/6b87ec6df6b1408d5af4ff79ec318365.png)](https://gyazo.com/6b87ec6df6b1408d5af4ff79ec318365)
- Q does not change

#### Load = 1
?
[![Image from Gyazo](https://i.gyazo.com/1f688c4fd3aa3cd710cd885e3df10418.png)](https://gyazo.com/1f688c4fd3aa3cd710cd885e3df10418)
Q becomes what D was during moment

### Components
- has input/output
- Load to determine whether on/off

###  function
- Has current state (0 or 1),  outputs
- When clock "ticks", value is input into clocked register, new state

### System-wide clock
- Sends pulses
- Clock period: 1 full cycle duration
- Clock frequency: 1/period

___
References:

Created:: 2022-03-27 00:54
