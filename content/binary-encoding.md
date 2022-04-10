---
title: Binary Encoding
aliases:
---
Status:
Tags: #aCards/cmpt295/binary 
Links: [Binary](out/binary.md)
___

# Binary Encoding

## Data Type Sizes
- One digits is saved for the sign !

| Data        | Size |
| ----------- | ---- |
| int         | 4    |
| long        | 8    |
| char        | 1    |
| float       | 4    |
| double      | 8    |
| long double | 12   |
- [Binary Float Byte Structure](out/binary-float-byte-structure.md)
- Floats byte structure
	- [![Image from Gyazo|700](https://i.gyazo.com/a976e15b77e3e7fd2702210d054a529e.png)](https://gyazo.com/a976e15b77e3e7fd2702210d054a529e)
	-

## Padding
- When shifting left, padding always ;;  0
<!--SR:!2022-02-18,2,150-->
- When shifting right ;; unsigned is 0, signed is 1
<!--SR:!2022-02-18,2,150-->
___

# Backlinks
```dataview
list from [Binary Encoding](out/binary-encoding.md) AND !outgoing([Binary Encoding](out/binary-encoding.md))
```
___
References:

Created:: 2021-09-29 14:36
