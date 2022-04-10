---
title: Condition Codes
aliases:
---
Status:
Tags: #cards/cmpt295/assembly
Links: [Central Processing Unit (CPU)](out/central-processing-unit-cpu.md)
___

# Condition Codes

## Principles
CF - Carry Flag (for unsigned)
?
- indicates whether there is overflow
<!--SR:!2022-04-11,25,150-->

ZF - Zero Flag
?
- if result is 0
<!--SR:!2022-04-03,17,130-->

SF - Sign Flag (for signed)
?
- indicates whether result is a -ve number
<!--SR:!2022-04-10,24,150-->

OF - Overflow Flag (for signed)
?
- indicates whether result creaed +ve or -ve overflow
<!--SR:!2022-04-03,17,130-->

### Changing

#### cmp\* and test\* set condition codes
Branching
?
- cmp\* instruction ;; compare
<!--SR:!2022-04-08,22,130-->
	- [![Image from Gyazo](https://i.gyazo.com/413b54162a61412135b65b301ce8b0d7.png)](https://gyazo.com/413b54162a61412135b65b301ce8b0d7)
	- doesn't save result
	- set condition codes based on src1-src2
- test\* instruction (test)
	- [![Image from Gyazo](https://i.gyazo.com/37cd75fb6e458869579446e3aa15814e.png)](https://gyazo.com/37cd75fb6e458869579446e3aa15814e)
	- result not stored in dest
	- set conditon codes based on src1 and src2
- $j^x$ instructions (jump)

#### $j^X$ use condition codes
?
[![Image from Gyazo](https://i.gyazo.com/6d49698402b09fdfd297aff6841470d2.png)](https://gyazo.com/6d49698402b09fdfd297aff6841470d2)
<!--SR:!2022-04-09,23,130-->

## Examples

### function with if/else and return
?
- Code false condition first
	- If false, jump, else do true
	- have jump after true to prevent false from running
[![Image from Gyazo](https://i.gyazo.com/f8cad5e2621570fe9960163a35017e0e.png)](https://gyazo.com/f8cad5e2621570fe9960163a35017e0e)
<!--SR:!2022-03-25,4,130-->

[![Image from Gyazo](https://i.gyazo.com/280880499cf36597cea01a22fd9feb86.png)](https://gyazo.com/280880499cf36597cea01a22fd9feb86)
___

# Backlinks
```dataview
list from [Condition Codes](out/condition-codes.md) AND !outgoing([Condition Codes](out/condition-codes.md))
```
___
References:

Created:: 2022-02-05 20:58
