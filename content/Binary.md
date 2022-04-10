---
title: Binary
aliases:
---
Status:
Tags: #archivedCards/macm101/numbertheory #aCards/cmpt295/binary
Links: [Nand2Tetris MOC](out/nand2tetris-moc.md)
___

# Binary

## Principles
Using 0's and 1's to represent digits
- [Binary Operations](out/binary-operations.md)
- [Binary Encoding](out/binary-encoding.md)
- [Negative Binary](out/negative-binary.md)

### General Form
`?`
[![Image from Gyazo](https://i.gyazo.com/20857d3e8690a809f6a9a1fe2339727a.png)](https://gyazo.com/20857d3e8690a809f6a9a1fe2339727a)
- Keep dividing quotient by 2, get remainder, and keep doing 
<!--SR:!2021-12-10,4,170-->

Find binary expansion of 165
`?`
[![Image from Gyazo](https://i.gyazo.com/ab8bf43ca7136f8ad76c1d824103b9c7.png)](https://gyazo.com/ab8bf43ca7136f8ad76c1d824103b9c7)
<!--SR:!2021-12-12,6,190-->

[![Image from Gyazo](https://i.gyazo.com/47980a926424018bf7af2ffeaa4b29c7.png)](https://gyazo.com/47980a926424018bf7af2ffeaa4b29c7)
## Examples

### Int in C
- Last one determines sign

| Decimal     | Binary                              |     |
| ----------- | ----------------------------------- | --- |
| -2147483648 | 10000000 00000000 00000000 00000000 |     |
| -2147483647 | 10000000 00000000 00000000 00000001 | ___ |

## Converting
Steps to convert negative number to binary
?
- Take positive form
- Negate it (0's become 1's, 1's become 0's)
- Add 1

Steps to convert signed to unsigned
?
- Add value of last binary digit

Steps to convert unsigned to signed
?
- Subtract value of last binary digit

## Exercises
1. Convert 10011011 from binary to decimal.
2. Convert 29 from decimal to binary.
3. Write a program that get an integer in decimal and print its binary form.
4.

# Backlinks
```dataview
list from [Binary](out/binary.md) AND !outgoing([Binary](out/binary.md))
```
___
References: