---
aliases:
---
Status:
Tags: #aCards/cmpt295/binary
Links: [[Binary]]
___

# Binary rounding rules

## Principles
- Worth of a bit is the value of 2x where x is associated with its position in the bit pattern, even though the bit itself may be 0

### Types
Identify bit at rounding position, and determine rounding type:

#### Round up
?
- sum of bits to right > half of rounding bit
	- ex) if rounding pos is worth 1/4, check if left is greater than 1/8
	- ex) **0**110 is round up
- Add 1 to the bit at rounding position, discard bits to the right
<!--SR:!2022-02-18,2,150-->

#### Round down
?
- sum of bits to right < half of rounding bit
	 - ex) **0**011 is round down
- DIscard bits
<!--SR:!2022-02-18,2,150-->

#### Round to even number
?
- If bits to right == bit at rounding
	- ex) **0**01 is round to even
- round such that the bit at the rounding position becomes 0
- If the bit at rounding position is 1 => then we round to even number by rounding up
	- Add 1 to left of position bit
- if the bit at rounding position is already 0 => then we round to even number by rounding down
<!--SR:!2022-02-17,1,130-->

### Rounding IEEE
- Positioned bit is 23rd bit

## Examples
Round [![Image from Gyazo](https://i.gyazo.com/8b55233d3cf0526a2a0ec0cad259405e.png)](https://gyazo.com/8b55233d3cf0526a2a0ec0cad259405e)
?
[![Image from Gyazo](https://i.gyazo.com/697c5f3e7679ea0373aa9ddff269032b.png)](https://gyazo.com/697c5f3e7679ea0373aa9ddff269032b)
___
<!--SR:!2022-02-17,1,130-->

# Backlinks
```dataview
list from [[Binary rounding rules]] AND !outgoing([[Binary rounding rules]])
```
___
References:

Created:: 2022-01-24 14:47
