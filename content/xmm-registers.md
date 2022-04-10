---
title: XMM Registers
aliases:
---
Status:
Tags: #cards/cmpt295/data
Links: [CPU Registers](out/cpu-registers.md) - [Floating Point Data](out/floating-point-data.md)
___

# XMM Registers

## Principles
?
- 16 in total, each 16-bytes wide
- named `%xmm0, ... %xmm15`
	- 0-7 are for parameters
	- 8-15 are for local data
- All are caller-saved
- Parameters are being passed into xmm
- Result is stored in xmm0
<!--SR:!2022-03-22,1,130-->

Can be used in tandem with regular bit registers
?
- [![Image from Gyazo](https://i.gyazo.com/eda379f226d39472561e627bd7c0086a.png)](https://gyazo.com/eda379f226d39472561e627bd7c0086a)
- Pointers and integers stored into bit
- Float registers passed into XMM
<!--SR:!2022-03-22,1,130-->

### Structure
[![Image from Gyazo](https://i.gyazo.com/7724cb1ad15833ec38364ad2ff38aaca.png)](https://gyazo.com/7724cb1ad15833ec38364ad2ff38aaca)
- Groups of registers, allows you to apply to all

## Scalar
Scalar mode and vector (packed) modes
- 1 single-precision float
- add`s`s vs add`p`s
	- `code` determines scalar vs vector
	- s determines single precision
- [![Image from Gyazo](https://i.gyazo.com/19233956a7b60f63856980a9c0703523.png)](https://gyazo.com/19233956a7b60f63856980a9c0703523)

### Converting values inside registers
[![Image from Gyazo](https://i.gyazo.com/76bd8187b9f56dd7ee05feaf5a915586.png)](https://gyazo.com/76bd8187b9f56dd7ee05feaf5a915586)
### Operations
Artihmetic
?
- s stands for single (int), d stands for double (double/64)
- addss
- subss
- mulss
- divss
<!--SR:!2022-03-22,1,130-->

Logical
?
- andps
- orps
- xorps
<!--SR:!2022-03-22,1,130-->

Comparison
?
- ucomiss
<!--SR:!2022-03-22,1,130-->

Math
?
- maxss
- minss
- sqrtss
<!--SR:!2022-03-22,1,130-->

___
References:

Created:: 2022-03-14 03:28
