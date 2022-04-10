---
title: MIPS
aliases:
---
Status:
Tags: #cards/cmpt295/isa 
Links: [Instruction Set Architecture (ISA)](out/instruction-set-architecture-isa.md)
___

# MIPS

## Principles
?
- 32 registers
- size of each register and word size is 32 bits
- size of memory adress is 32 bits
- Memory size is $2^32$ x 8

### Registers
[![Image from Gyazo](https://i.gyazo.com/83b72bc484421d365fd183dc7845b8a3.png)](https://gyazo.com/83b72bc484421d365fd183dc7845b8a3)

### Memory Model
?
[![Image from Gyazo](https://i.gyazo.com/a01b58acac37a72743d8613e2845b432.png)](https://gyazo.com/a01b58acac37a72743d8613e2845b432)
- `tx` registers are not presrved, while `sx` are
<!--SR:!2022-03-22,1,130-->

### Instruction Set
- 3 operand assembly language
- Only having 3 operands for all instruction make microprocessor hardware easy

#### Instructions
lw `reg`, `M`
sw `reg`, `M`
add `dest`, `a`, `b`
sub `dest`, `a`, `b`
mul `dest`, `a`, `b`

#### Example of Assembly to Machine
[![Image from Gyazo](https://i.gyazo.com/98ddaf36e051f1cf30fe7590a855d2ab.png)](https://gyazo.com/98ddaf36e051f1cf30fe7590a855d2ab)
#### Layout
`opcode` ; operation of instruction (6)
`rs` ; first register (5)
`rt` ; second register source operand (5)
`rd` ; register destination operand (5)
`shamt` ; shift amount (6)
`func` ; function (code), variant of operation in opcode field

- 32 registers so 5 bits can help reach all indexes

#### Instruction Layouts
[![Image from Gyazo](https://i.gyazo.com/ded5025bd7908c9489cf267d8c37ae64.png)](https://gyazo.com/ded5025bd7908c9489cf267d8c37ae64)
- opcode determines instruction + format of instruction to differentiate between the formats
- 
___
References:

Created:: 2022-03-15 19:59
