---
title: Negative Binary
aliases:
---
Status:
Tags: #aCards/cmpt295/binary 
Links: [Binary](out/binary.md)
___

# Negative Binary
To accomodate for negative numbers, the total storage is split and categorized based on the nth bus
`-x = (2^n)-x`


- 1st bit on implies negative of capacity, rest are positive and negate it

[![Image from Gyazo](https://i.gyazo.com/7bf850e50c4f663015da3a9ad639f3d4.png)](https://gyazo.com/7bf850e50c4f663015da3a9ad639f3d4)

## 15-Bit Example
| Binary | Number | 2's Complement |
| ------ | ------ | -------------- |
| 0000   | 0      | 0              |
| 0001   | 1      | 1              |
| 0111   | 8      | 8              |
| 1000   | -8     | 9              |
- This natural composition makes subtraction possible using [ Binary Addition](out/binary-operations.md)

### Two's Complement to Binary
?
- Add $2^n$ to signed to get unsigned
[![Image from Gyazo](https://i.gyazo.com/190e1808d75411b847e8f1e738483c3b.png)](https://gyazo.com/190e1808d75411b847e8f1e738483c3b)
<!--SR:!2022-02-17,1,130-->

### Binary to Two's Complement
?
- Flip bits and add 1
- Makes sense since max of negative is 2^n, but max of pos is 2^n-1
[![Image from Gyazo](https://i.gyazo.com/d724d3b0951a38466e3ed0e91140ed31.png)](https://gyazo.com/d724d3b0951a38466e3ed0e91140ed31)
___
References: